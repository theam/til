Gonzalo García

# Port Scanning with netcat

MacOS High Sierra (10.13) removed the telnet command but we can use netcat to scan ports too:

Syntax:

```bash
nc -vz <host> [port]
```

*Example*:

Single port:

```bash
nc -vz google.es 80
```

Range:
```bash
nc -vz google.es 80-90
```
