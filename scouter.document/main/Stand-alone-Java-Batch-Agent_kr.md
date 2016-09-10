# Stand-alone Java Batch Agent

��ī���� APM�� WAS �Ӹ� �ƴ϶� ��ġ ����͸� ��ɵ� �����Ѵ�.
��ġ�� �Ϲ������� �뷮 ���� ó���ϴ� ��찡 ���� �Ϲ� APM���δ� ����͸��� �Ѱ谡 �־���. ��ī���ʹ� ��ġ Ư���� ����Ͽ� ��� �߽����� ������ �м������� �ڹ� �Լ� �������� �м��� �� �ִ�.

��ī���� ��ġ ������Ʈ�� �Ʒ��� ���� ����� �����Ѵ�.
- ����ð� ����(CPU ��뷮)
- SQL �������ϸ�(SQL��, SQL ����ð�, SQL ó���Ǽ�, SQL ����Ƚ��)
- �ֱ����� ���μ��� ���� ����  

## �ڹ� �ɼ�
��ī���� ��ġ ������Ʈ�� �⺻ ��ġ ����� WAS ��� �ڹ� ������Ʈ�� �����ϴ�.
�ڹ� ��ġ ���� ���(�� ��ũ��Ʈ ����)�� -javaagent�� -Dscouter.config ������ �߰��ϸ� ����͸��� �����ϴ�.

```
JAVA_OPTS=" ${JAVA_OPTS} -javaagent:${SCOUTER_AGENT_DIR}/scouter.agent.batch.jar"
JAVA_OPTS=" ${JAVA_OPTS} -Dscouter.config=${SCOUTER_AGENT_DIR}/scouter.batch.conf"
```

## ȯ�漳��

### ȯ�漳�� ����
`${SCOUTER_AGENT_DIR}/scouter.batch.conf` ���� ȯ�漳�� ������ �����ϰ�, ������ ���������ν� ���� �ɼ��� ������ �� �ִ�.
> �ɼ��� ������ �⺻ ���� ����ȴ�.

##### ��
*${appropriate_directory}/scouter.conf*
```
# Stand-Alone mode
scouter_standalone=false

# Batch ID (batch_id_type: class,args,props) (batch_id: args->index number, props->key string)
batch_id_type=args
batch_id=0

# Scouter Server IP Address (Default : 127.0.0.1)
net_collector_ip=127.0.0.1

# Scouter Server Port (Default : 6100)
net_collector_udp_port=6100
net_collector_tcp_port=6100

# Scouter Name(Default : batch)
obj_name=exbatch
```
For more options, refer Options page(Coming soon).
***



![login](../img/main/live-demo-client-login.png)