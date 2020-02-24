### Step 1 : Set accept all policy to all connections
Using below set of command you will set accept rule for all type of connections.
 
```bash
# iptables -P INPUT ACCEPT
# iptables -P OUTPUT ACCEPT
# iptables -P FORWARD ACCEPT
```
 
This will confirm, iptables gonna accept all requests for all type of connections.

### Step 2 : Delete all existing rules.

Using below set of commands, delete your currently configured rules from iptables.

```bash
# iptables -F
```
