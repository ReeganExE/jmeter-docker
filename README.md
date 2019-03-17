# Apache JMeter Base Image

This base image could help you build an [Apache JMeter Distributed Testing](https://jmeter.apache.org/usermanual/jmeter_distributed_testing_step_by_step.html) with Docker.

JMeter binaries are already in `$PATH`. Just extend and input your command.

See more at [jmeter-distributed-testing](https://github.com/ReeganExE/jmeter-distributed-testing).

Example

### Slaves

```Dockerfile
FROM reeganexe/jmeter

CMD ["jmeter-server"]
```

### Master

```Dockerfile
FROM reeganexe/jmeter

CMD ["jmeter", "-R", "10.2.3.4,10.2.3.5"]
```

Check out [jmeter-distributed-testing](https://github.com/ReeganExE/jmeter-distributed-testing) for JMeter auto-discovery slaves.
