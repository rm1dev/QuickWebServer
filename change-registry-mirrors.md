برای رفع مشکل تحریم داکر دستور زیر را اجرا کنید:

```sh
vi /etc/docker/daemon.json
```

در این فایل کد زیر را وارد کنید:

```sh
{
   "registry-mirrors": ["https://docker.iranrepo.ir", "https://dockerhub.ir", "https://registry.docker.ir", "https://docker.host:5000"]
}
```

بعد از اضافه کردن کد بالا به فایل daemon.json این فایل را ذخیره کنید و بعد دو دستور زیر را اجرا کنید:

```sh
systemctl daemon-reload
systemctl restart docker
```

حالا مشکل شما با تحریم داکر حل خواهد شد.