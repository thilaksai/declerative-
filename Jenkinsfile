pipeline
{
 agent Jenkins
  stages
   {
     stage('clone')
      {
       steps
        {
         git 'https://github.com/thilaksai/declerative-.git'
	} 
      }
        stage('compile')
      {
       steps
        {
         sh 'mvn clean compile'
        }
      }
         stage('ccode review')
      {
       steps
        {
         sh  'mvn clean pmd:pmd'
        }
      } 
        stage('unit test')
        {  
         steps
          {
            sh 'mvn clean test'
          }            
        }
       stage('code coverage')
         {
          steps
           {
                 sh 'mvn clean cobertura:check'
           }   
        } 
      stage('install')
       {
        steps
          {
            sh 'mvn clean install'
          }
       }  
  }

}  
