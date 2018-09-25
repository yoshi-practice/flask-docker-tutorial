# FlaskTutorial

It is Flask tutorial repository.

---

### Version

```
$ docker --version
```

---

### Local directory

```
.
├── Dockerfile
├── hello.py
└── requirements.txt
```

---

### requirements.txt

It is the same as the one created in the following way.

```
$ pip install flask
$ pip freeze > requirements.txt
```

If you can change the version of the package you may do

```
$ pip install flask
```

---

### hello.py

Use the official page code.
But, only the argument of `app run` is changed to the original code.

---

### Create image

```
$ cd /path/to/flask/
$ docker build -t flask . 
```

- `-t flask` : Image named `flask`
- `.` : Use Docker file at current directory.

---

### Start Container

```
$ docker run -p 5000:5000 -it flask /bin/sh
```

- `-p 5000:5000` : hostの5000番ポートをコンテナの5000番ポートに向ける
- `-it` : 現在の入力デバイスでコンテナを操作
- `flask` : イメージ名の指定
- `/bin/sh` : 起動したコンテナでshコマンドを実行
