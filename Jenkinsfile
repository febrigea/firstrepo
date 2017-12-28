// Declarative //
pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				bat 'make'
			}
		}
		stage('Test') {
			steps {
				bat 'make check'
				junit 'reports/**/*.xml'
			}
		}
		stage('Deploy') {
			steps {
				bat 'make publibat'
			}
		}
	}
}
// Script //
node {
	stage('Build') {
		bat 'make'
	}
	stage('Test') {
		bat 'make check'
		junit 'reports/**/*.xml'
	}
	stage('Deploy') {
		bat 'make publibat'
	}
}