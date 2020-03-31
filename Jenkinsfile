node {

    stage('Git clone configuration-service') {
          git 'https://github.com/TheLibraryGroup/configuration-service.git'
        }

        stage('Maven package'){
            def mvnHome = tool name: 'maven', type: 'maven'
            sh "${mvnHome}/bin/mvn -f pom.xml package"
        }

        stage('SSH publisher configuration-service'){
            sshPublisher(
                publishers: [
                    sshPublisherDesc(
                        configName: 'vps778813.ovh.net',
                        transfers: [
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[, ]+',
                                remoteDirectory: '/docker/thelibrary-group/',
                                remoteDirectorySDF: false,
                                removePrefix: 'docker',
                                sourceFiles: '../docker/back/configuration-service-0.0.1-SNAPSHOT.jar'
                            ),
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[,]+',
                                remoteDirectory: '/docker/thelibrary/back',
                                remoteDirectorySDF: false,
                                removePrefix: '',
                                sourceFiles: 'Dockerfile-configuration'
                            ),
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[,]+',
                                remoteDirectory: '/docker/thelibrary',
                                remoteDirectorySDF: false,
                                removePrefix: '',
                                sourceFiles: 'docker-compose.yml'
                            )
                        ],
                        usePromotionTimestamp: false,
                        useWorkspaceInPromotion: false,
                        verbose: false
                    )
                ]
            )
        }

        stage('Clean workspace'){
            cleanWs()
        }

    stage('Git clone discovery-service') {
              git 'https://github.com/TheLibraryGroup/discovery-service.git'
        }

        stage('Maven package'){
            def mvnHome = tool name: 'maven', type: 'maven'
            sh "${mvnHome}/bin/mvn -f pom.xml package"
        }

        stage('SSH publisher discovery-service'){
            sshPublisher(
                publishers: [
                    sshPublisherDesc(
                        configName: 'vps778813.ovh.net',
                        transfers: [
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[, ]+',
                                remoteDirectory: '/docker/thelibrary-group/',
                                remoteDirectorySDF: false,
                                removePrefix: 'docker',
                                sourceFiles: '../docker/back/discovery-service-0.0.1-SNAPSHOT.jar'
                            ),
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[,]+',
                                remoteDirectory: '/docker/thelibrary/back',
                                remoteDirectorySDF: false,
                                removePrefix: '',
                                sourceFiles: 'Dockerfile-discovery'
                            ),
                        ],
                        usePromotionTimestamp: false,
                        useWorkspaceInPromotion: false,
                        verbose: false
                    )
                ]
            )
        }

        stage('Clean workspace'){
            cleanWs()
        }

    stage('Git clone gateway-service') {
              git 'https://github.com/TheLibraryGroup/gateway-service.git'
        }

        stage('Maven package'){
            def mvnHome = tool name: 'maven', type: 'maven'
            sh "${mvnHome}/bin/mvn -f pom.xml package"
        }

        stage('SSH publisher gateway-service'){
            sshPublisher(
                publishers: [
                    sshPublisherDesc(
                        configName: 'vps778813.ovh.net',
                        transfers: [
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[, ]+',
                                remoteDirectory: '/docker/thelibrary-group/',
                                remoteDirectorySDF: false,
                                removePrefix: 'docker',
                                sourceFiles: '../docker/back/gateway-service-0.0.1-SNAPSHOT.jar'
                            ),
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[,]+',
                                remoteDirectory: '/docker/thelibrary/back',
                                remoteDirectorySDF: false,
                                removePrefix: '',
                                sourceFiles: 'Dockerfile-gateway'
                            ),
                        ],
                        usePromotionTimestamp: false,
                        useWorkspaceInPromotion: false,
                        verbose: false
                    )
                ]
            )
        }

        stage('Clean workspace'){
            cleanWs()
        }

    stage('Git clone book-service') {
             git 'https://github.com/TheLibraryGroup/microservice-book.git'
        }

        stage('Maven package'){
            def mvnHome = tool name: 'maven', type: 'maven'
            sh "${mvnHome}/bin/mvn -f pom.xml package"
        }

        stage('SSH publisher book-service'){
            sshPublisher(
                publishers: [
                    sshPublisherDesc(
                        configName: 'vps778813.ovh.net',
                        transfers: [
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[, ]+',
                                remoteDirectory: '/docker/thelibrary-group/',
                                remoteDirectorySDF: false,
                                removePrefix: 'docker',
                                sourceFiles: '../docker/back/microservice-book-0.0.1-SNAPSHOT.jar'
                            ),
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[,]+',
                                remoteDirectory: '/docker/thelibrary/back',
                                remoteDirectorySDF: false,
                                removePrefix: '',
                                sourceFiles: 'Dockerfile-ms-book'
                            ),
                        ],
                        usePromotionTimestamp: false,
                        useWorkspaceInPromotion: false,
                        verbose: false
                    )
                ]
            )
        }

        stage('Clean workspace'){
            cleanWs()
        }


    stage('Git clone frontend') {
          git 'https://github.com/TheLibraryGroup/angular-app.git'
        }
        stage('SSH publisher front'){
            sshPublisher(
                publishers: [
                    sshPublisherDesc(
                        configName: 'vps778813.ovh.net',
                        transfers: [
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[, ]+',
                                remoteDirectory: '/docker/thelibrary/front',
                                remoteDirectorySDF: false,
                                removePrefix: '',
                                sourceFiles: '**/*'
                            ),
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: 'cp /etc/letsencrypt/live/jenkins.mypoc.online/fullchain.pem /opt/docker/thelibrary/build/front/ssl/fullchain.pem && cp /etc/letsencrypt/live/jenkins.mypoc.online/privkey.pem /opt/docker/thelibrary/build/front/ssl/privkey.pem',
                                execTimeout: 300000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[, ]+',
                                remoteDirectory: '/docker/thelibrary',
                                remoteDirectorySDF: false,
                                removePrefix: '',
                                sourceFiles: ''
                            ),
                            sshTransfer(
                                cleanRemote: false,
                                excludes: '',
                                execCommand: '',
                                execTimeout: 120000,
                                flatten: false,
                                makeEmptyDirs: false,
                                noDefaultExcludes: false,
                                patternSeparator: '[,]+',
                                remoteDirectory: '/docker/thelibrary/front',
                                remoteDirectorySDF: false,
                                removePrefix: '',
                                sourceFiles: 'Dockerfile-gateway'
                            ),
                        ],
                        usePromotionTimestamp: false,
                        useWorkspaceInPromotion: false,
                        verbose: false
                    )
                ]
            )
        }


}
