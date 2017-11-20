# awslogs-config

![Build Status](https://travis-ci.org/traveloka/ansible-awslogs-config.svg?branch=master)

Setup awslogs config

## Requirements

awslogs is installed

## Role Variables
- awslogs_agent_conf_dir: awslogs config directory.

  the default is /etc/awslogs/conf.d
- awslogs_app_name: what to name the generated config

  e.g. "traveloka" -> the generated config will be saved in "{{ awslogs_agent_conf_dir }}/traveloka.conf"

- awslogs_app_log_settings: array of [CloudWatch logs settings](http://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/AgentReference.html)
  - group_name: the target group name in AWS CWL
  - stream_name: the target stream name in AWS CWL. default to hostname
  - see the official documentation for other available options

## Dependencies

None

## Example Playbook

```
- role: "awslogs-config"
  awslogs_app_log_settings:
    - file: "/var/log/nginx/access.log"
      datetime_format: "%Y/%m/%d %H:%M:%S.%f"
      group_name: "nginx.access.log"
      time_zone: "UTC"
```

## License

MIT

## Author Information

[Salvian Reynaldi](https://github.com/SalzzZ)
