// Related to https://issues.jenkins-ci.org/browse/JENKINS-26481

abcs = [ '/prod/NorthAmericaClaims/USClaims/DG_Monitor_Test/Folder A',
        '/prod/NorthAmericaClaims/USClaims/DG_Monitor_Test/Folder B',
        '/prod/NorthAmericaClaims/USClaims/DG_Monitor_Test/Folder C',
        '/prod/NorthAmericaClaims/USClaims/DG_Monitor_Test/Folder D',
        '/prod/NorthAmericaClaims/USClaims/DG_Monitor_Test/Folder E',
        '/prod/NorthAmericaClaims/USClaims/DG_Monitor_Test/Folder F',
        '/prod/NorthAmericaClaims/USClaims/DG_Monitor_Test/Folder G',
]

node('master') {
    stage('ADDING Service Checks to Nagios') {
        echo_all(abcs)
}
}

@NonCPS // has to be NonCPS or the build breaks on the call to .each
def echo_all(list) {
    list.each { item ->
        echo "Hello Hi ${item}"
    }
}
// outputs all items as expected

// @NonCPS
// def loop_of_sh(list) {
//    list.each { item ->
//        sh "echo Hello ${item}"
//    }
//}
// outputs only the first item

//@NonCPS
//def loop_with_preceding_sh(list) {
//    sh "echo Going to echo a list"
//    list.each { item ->
//        sh "echo Hello ${item}"
 //   }
//}
// outputs only the "Going to echo a list" bit

// echoes everything as expected
