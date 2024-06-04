pipeline
{
  agent any
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
            println " Estoy en " + ciudad + "que tiene " + habitantes + "habitantes y hace un dia " + clima
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
  }
  post
  {
    always
    {
        echo "El pipeline se está ejecutando."
    }
  
  }
}
