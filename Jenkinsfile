node {
   stage 'Checkout'
   git url: 'https://github.com/accelaerodev/example-continuous-delivery.git'

   stage 'Build'
   sh "./gradlew build"
   
   stage 'Docker'
   sh "./gradlew buildDocker"
}
