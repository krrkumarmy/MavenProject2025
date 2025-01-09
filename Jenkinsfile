pipeline
{
agent any
stages
{

stage("SCM checkout")
{steps{git branch: 'master', url: 'https://github.com/krrkumarmy/MavenProject2025.git'}}

stage("code validate")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn validate'}}
}

stage("code Compile")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn compile'}}
}

stage("Test")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn test'}}
}


stage("Package creation")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn package'}}
}

stage("Verify step")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn verify'}}
}

stage("insall")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn clean install -DskipTests'}}
}

stage("deploy the artificats to Dev server")
{steps{sshagent(['Deploy2Jboss'])
{
  sh 'scp -o StrictHostKeyChecking=no webapp/target/webapp.war ec2-user@172.31.20.39:/opt/wildfly'
}
}

}
}
}

