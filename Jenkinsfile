pipeline
{
    agent any

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
    }
}