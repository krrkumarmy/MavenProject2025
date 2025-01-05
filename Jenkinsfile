pipeline
{
agent any
stages
{
stage("SCM checkout")
{steps{git branch: 'master', url: 'https://github.com/krrkumarmy/MavenProject2025.git'}}

stage("code validate ")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn validate'}}
}

stage("code validate ")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn compile'}}

stage("code validate ")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn test'}}
}
}

}}