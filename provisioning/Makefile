server:
	ansible-playbook server.yml -i hosts.yml

authorize:
	ansible-playbook athorize.yml -i hosts.yml

authorize-agents:
	ansible-playbook athorize-agents.yml -i hosts.yml

generate-agent-key:
	ssh-keygen -q -t rsa -N '' -f files/agent_rsa

upgrade:
	ansible-playbook upgrade.yml -i hosts.yml

show-initial-password:
	ansible -i hosts.yml manager -m shell -a 'cd /home/deploy/jenkins && docker-compose exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword'