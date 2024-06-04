pipeline
{
  agent any
  environment
  {
    USUARIO = "${currentBuild.getBuildCauses()[0].userId}"
  }
  stages
  {
    stage("Informacion ciudad")
    {
      steps
      {
        script
        {
            ciudad = "Madrid"
            habitantes = 3332035
            clima = "soleado"
            println " Estoy en " + ciudad + " que tiene " + habitantes + " habitantes y hace un dia " + clima
        }
      }
    }
    stage("Ejecutar comando")
    {
      steps
      {
        bat "cmd ipconfig /flushdns"
      }
    }
    stage("Usuario que ejecuta pipeline")
    {
      steps
      {
        script
        {
          echo "La tarea la ejecutó ${env.USUARIO}"
        }
      }
    }
  }
  post
  {
    always
    {
        echo "El pipeline se esta ejecutando."
    }
  
  }
}
