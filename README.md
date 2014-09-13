Vagrant AWS Test
================

먼저 AWS Provider를 위한 더미 Vagrant Box를 추가해야 한다.

```shell
$ vagrant box add dummy https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box
```

다음과 같이 초기화하고, `Vagrantfile`을 편집한다.

```shell
$ vagrant init dummy
```

다음과 같은 환경 변수를 사용하므로 환경 변수를 추가해서 사용하자.

```shell
$ export AWS_ACCESS_KEY_ID=
$ export AWS_SECRET_ACCESS_KEY_ID=
$ export AWS_KEYPAIR_NAME=
$ export AWS_PRIVATE_KEY_PATH=
```

최초 실행 시에는 `--provider=aws` 옵션을 반드시 추가해야 한다.

```shell
$ vagrant up --provider=aws
```

인스턴스에 SSH로 접속하기 위해서는 다음과 같이 실행한다.

```shell
$ vagrant ssh
```

마찬가지로 인스턴스를 정지하거나 삭제할 수 있다.

```shell
$ vagrant halt
$ vagrant destroy
```
