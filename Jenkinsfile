node {
   stage 'Checkout'
   git url: 'https://github.com/accelaerodev/example-continuous-delivery.git'

   stage 'Build'
   sh "./gradlew build"
   
   stage 'Docker Image'
   sh "./gradlew buildDocker"

   stage 'Push to Registry'
   sh "docker tag accelaero/example-continuous-delivery localhost:5002/example-continuous-delivery:latest"
   sh "docker push localhost:5002/example-continuous-delivery:latest"
}
