properties([
	pipelineTriggers([pollSCM('H/3 * * * *')])
	])

node() {
	docker.image('gcc:4.9').inside {
		cleanWs()
		checkout scm
		sh "make"
		sh "./main"
	}
}
