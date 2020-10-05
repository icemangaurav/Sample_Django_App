#!groovy

node {

    try {
        stage 'Checkout'
            checkout scm

            sh 'git clone https://github.com/icemangaurav/Sample_Django_App.git'
            
            

        stage 'Test'
            sh '''
            python3 -m pip install --user --upgrade pip
            python3 -m pip install --user virtualenv
            virtualenv env -p python3.7
            . env/bin/activate
            env/bin/pip install -r requirements.txt'''
            

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
