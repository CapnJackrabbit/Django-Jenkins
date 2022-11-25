pipeline
{
    agent
    {
        docker
        {
            image 'python:3.11'
            args '-u root:root'
        }
    }

    stages
    {
        stage('Validações')
        {
            steps
            {
                sh 'python -V'
            }
        }

        stage('Instalando itens de requisitos')
        {
            steps
            {
                sh 'pip install -r requisitos.txt'
            }
        }

        stage('Validando o código')
        {
            steps
            {
                sh 'find . -name \\*py | xargs pylint -f parseable | tee pylint.log'
                sh 'find . -name \\*py | xargs pycodestyle | tee pep8.log'
            }
        }
    }
}