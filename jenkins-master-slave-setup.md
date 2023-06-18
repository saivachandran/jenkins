# jenkins master slave setup url refrence

[link1](https://www.linkedin.com/pulse/jenkins-masterslave-setup-prayag-sangode)

[videolink](https://www.youtube.com/watch?v=fphtfmAsfhU)


# run jenkins agent background

sudo vim /etc/systemd/system/jenkins-agent.service

[Unit]
Description=Jenkins Agent

[Service]
ExecStart=/usr/bin/java -jar /path/to/agent.jar -jnlpUrl https://devjen.domain.in/computer/slavenode1/jenkins-agent.jnlp -secret @secret-file -workDir "/home/user"

[Install]
WantedBy=multi-user.target

```
sudo systemctl enable jenkins-agent
sudo systemctl start jenkins-agent
```

