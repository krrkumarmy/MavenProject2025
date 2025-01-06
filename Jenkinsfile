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
<<<<<<< HEAD
=======

>>>>>>> a5187fc940d2b8399cf5c9bb0771bce4ae7b264d
stage("Test")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn test'}}
}
<<<<<<< HEAD

stage("Package creation")
{steps{withMaven(globalMavenSettingsConfig: '', jdk: 'Java_home', maven: 'maven_home', mavenSettingsConfig: '', traceability: true) 
{ sh 'mvn package'}}
}

}

}
=======

}}
>>>>>>> a5187fc940d2b8399cf5c9bb0771bce4ae7b264d
