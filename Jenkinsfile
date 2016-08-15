node {
   stage 'Checkout'
   git url: 'https://github.com/accelaerodev/example-continuous-delivery.git'

   stage 'Code Quality'
   sh "./gradlew pmdMain pmdTest pmdIntegrationTest"

   stage 'Compile Source'
   sh "./gradlew assemble"

   stage 'Unit Tests'
   sh "./gradlew test"
 
   stage 'Integration Tests'
   sh "./gradlew integrationTest"
   
   stage 'Docker Image'
   sh "./gradlew buildDocker"

   stage 'Push to Registry'
   sh "docker tag accelaero/example-continuous-delivery localhost:5002/example-continuous-delivery:latest"
   sh "docker push localhost:5002/example-continuous-delivery:latest"      

   stage 'Pull Image'
   sh "docker pull localhost:5002/example-continuous-delivery:latest"
}
