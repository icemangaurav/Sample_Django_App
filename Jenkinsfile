#!groovy

node {

    try {
        stage 'Checkout'
            checkout scm

            sh 'git clone https://github.com/icemangaurav/Sample_Django_App.git'
            
            

        stage 'Test'
            sh 'virtualenv env -p python3.7'
            sh '. env/bin/activate'
            sh 'env/bin/pip install -r requirements.txt'
            

        stage 'Deploy'
            echo "Deployent step executed"

        stage 'Publish results'
            echo "Results published"
            
    }

    catch (err) {
        
        echo "Exception throw"n
        throw err
    }

}