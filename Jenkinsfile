pipeline {
    agent any

    stages {
        stage('Check disk usage') {
            steps {
                echo 'Текущее состояние дисков:'
                sh '''
                    echo "=== df -h ==="
                    df -h
                '''
            }
        }

        stage('Process with max memory usage') {
            steps {
                echo 'Процесс, занимающий больше всего памяти:'
                sh '''
                    echo "=== TOP memory process ==="
                    ps aux --sort=-%mem | head -n 2
                '''
            }
        }
    }
}
