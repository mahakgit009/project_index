pipeline{
    agent{
        label{
		    label 'built-in'
		}	
	}
	stages{
	    
		stage ('master'){
		        steps{
				    sh "sudo yum install httpd -y"
					sh "sudo service httpd start"
					sh "sudo cp -r index.html /var/www/html"
					sh "sudo chmod -R 777 /var/www/html/index.html"
					
				}
		}
		stage ('node-1'){
            
			agent{
              
			    label{
		            
					label "172.31.42.35"
		        }	
	        }
			
			steps{
			      sh "sudo yum install httpd -y"
					sh "sudo service httpd start"
					sh "sudo cp -r index.html /var/www/html"
					sh "sudo chmod -R 777 /var/www/html/index.html"
			}
    		
		}
		stage ('node-2'){
            
			agent{
              
			    label{
		             label "172.31.45.219"
		        }	
	        }
			steps{
			        sh "sudo yum install httpd -y"
				    sh "sudo service httpd start"
				 	sh "sudo cp -r index.html /var/www/html"
					sh "sudo chmod -R 777 /var/www/html/index.html"
			}
    		
		}
        stage ('node-3'){
            
			agent{
              
			    label{
		             label "172.31.35.156"
		        }	
	        }
			steps{
			        sh "sudo yum install httpd -y"
				    sh "sudo service httpd start"
				 	sh "sudo cp -r index.html /var/www/html"
					sh "sudo chmod -R 777 /var/www/html/index.html"
			}
    		
		}
	}
}