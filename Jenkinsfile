#PIPELINE SCRIPT(GROOVY SCRIPT)
pipeline{
    agent any
    stages{
        stage('CHECKOUT'){
            steps{
                git 'https://github.com/VIJAYPRAKASH088/java-project-maven-new.git'
            }
        }
        stage('Compile'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
         stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.7.0.1746:sonar'
                }
            }
        }
        stage('Artifacts'){
            steps{
                sh 'mvn clean package'
            }
        }
        stage('Upload to S3'){
            steps{
                s3Upload consoleLogLevel: 'INFO', dontSetBuildResultOnFailure: false, dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 'pipeline-s3-publisher', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: false, noUploadOnFailure: false, selectedRegion: 'ap-south-1', showDirectlyInBrowser: false, sourceFile: '**/*.war', storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 's3creds', userMetadata: []
            }
        }
        stage('Deploy'){
            steps{
                deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'tomcatcreds', path: '', url: 'http://3.110.127.151:8080/')], contextPath: 'mywebapp', war: '**/*.war'
            }
        }
    }
}
