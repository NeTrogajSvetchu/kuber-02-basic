# kuber-02-basic

------

### Задание 1.

#### 1. Создал файл
   
   ![alt text](png/1.png)
   
```
apiVersion: v1
kind: Pod
metadata:
  name: hello-world
spec:
  containers:
  - name: echoserver
    image: gcr.io/kubernetes-e2e-test-images/echoserver:2.2
    ports:
    - containerPort: 8080
```
[helloworld.yaml](yaml/helloworld.yaml)
#### 2. Запуск "пода".
   
![alt text](png/2.png)

#### 3. Проброс портов

 Ввожу команду 

```
kubectl port-forward -n default pod/hello-world  8080:8080
```

![alt text](png/4.png)

#### Итоговый вывод curl

![alt text](png/3.png)


------

### Задание 2.

#### Создал новый под и сервис

![alt text](png/7.png)

[netolgysvc.yaml](yaml/netolgysvc.yaml)

[netologyweb.yaml](yaml/netologyweb.yaml)

#### Подключился и проверил

![alt text](png/5.png)

![alt text](png/6.png)
------

p.s

![alt text](png/8.png)