# java.security.policy

```
-Djava.security.manager
-Djava.security.debug="access,failure"
-Djava.security.policy=/path/to/java-security-policy/jadx.policy
```

## jadx

```sh
env JAVA_OPTS='-Djava.security.manager -Djava.security.debug="access,failure" -Djava.security.policy=/path/to/java-security-policy/jadx.policy' \
    /opt/jadx/bin/jadx-gui
```

## ghidra

> /opt/ghidra/support/launch.properties

```
VMARGS=-Djava.security.manager
VMARGS=-Djava.security.debug="access,failure"
VMARGS=-Djava.security.policy=/path/to/java-security-policy/ghidra.policy
```

## zap

```sh
sudo sed -i 's/exec java/exec java -Djava.security.manager -Djava.security.debug="access,failure" -Djava.security.policy=\/path\/to\/java-security-policy\/zap.policy/g' /opt/zap/zap.sh
```
