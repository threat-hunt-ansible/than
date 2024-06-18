# Detections
TODO

## Metadata

## Indicator types

## Detection output

## Detection script

## Example
```
- metadata:
    label: 'Scheduled Task/Job: Systemd Timers'
    description: 'Detect systemd timers'
    subtechniques:
      - T1053.006
    techniques:
      - T1053
    tactics:
      - TA0002
      - TA0003
      - TA0004
    author: 'Red Hat Information Security'
    version: '1'
    date: '2024-04-20'
  indicators:
    - content
    - domain
    - filename
    - ip
  detection:
    type: 'shell'
    executable: '/bin/bash'
    script: |
      2>/dev/null find /etc/systemd/ -type f -name "*.timer"
      2>/dev/null find /run/systemd/system/ -type f -name "*.timer"
      2>/dev/null find /usr/lib/systemd/ -type f -name "*.timer"
```
