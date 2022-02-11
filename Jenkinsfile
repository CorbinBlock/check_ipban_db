pipeline {
    agent none
    stages {
        stage('check_sqlite_db') {
            agent {
                label 'WIN-01-LENOVO'
            }
            steps {
                pwsh("""
                Set-Location \$env:python
                Set-Location sqlite
                python check_ipban_logs.py
                """)
            }
        }
        stage('check_sqlite_db_asus') {
            agent {
                label 'WIN-02-ASUS'
            }
            steps {
                pwsh("""
                Set-Location \$env:python
                Set-Location sqlite
                python check_ipban_logs.py
                """)
            }
        }
    }
}