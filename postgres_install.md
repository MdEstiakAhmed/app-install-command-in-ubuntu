`user@user:~$`
```
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
```

```
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
```

```
sudo apt-get update
```

```
sudo apt-get -y install postgresql
```

```
systemctl start postgresql.service
```

```
systemctl status postgresql.service
```

```
systemctl enable postgresql.service
```

```
sudo -i -u postgres
```


postgres@user:~$ 

```
psql
```

postgres=# 
```
create user testuser with password '12345';
```
```
create database test;
```
```
grant all privileges on database test to testuser;
```
```
\q
```

postgres@Estiak:~$ 
```
exit
```