Reproduces https://github.com/kevinconway/rpmvenv/issues/48

Run:
```shell
docker run -it --rm -v `pwd`:/opt/test centos:7

cd /opt/test
yum install -y python python-setuptools rpm-build
easy_install pip
pip install virtualenv rpmvenv

rpmvenv --verbose rpm.json
```
