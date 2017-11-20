# awslogs

![Build Status](https://travis-ci.org/traveloka/ansible-awslogs-config.svg?branch=master)

Setup awslogs config

## Requirements

awslogs is installed

## Role Variables

_TODO_

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
