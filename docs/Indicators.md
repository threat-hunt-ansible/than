# Indicators
TODO

## Indicator Types
- `content`
- `domain`
- `filename`
- `sha1`
- `sha256`
- `ip`

## Example
```
# Deleted binary
- metadata:
    label: 'BPFDoor Binary'
    description: 'Path of the binary which is deleted after execution'
    subtechniques:
      - T1070.004
    techniques:
      - T1070
    tactics:
      - TA0005
  type:
    - 'content'
  indicator: '/dev/shm/kdmtmpflush'

# Process Masquerading
- metadata:
    label: 'BPFDoor Masqueraded processes'
    description: 'Known processes bpfdoor is spoofing'
    subtechniques:
      - T1036.005
    techniques:
      - T1036
    tactics:
      - TA0005
  type:
    - 'content'
  indicator:
    - '/sbin/udevd -d'
    - '/sbin/mingetty /dev/tty7'
```
