### Introduction

- Fork this repo to build your own image with ERPNext and list of custom Frappe apps.
- Change `nginx/Dockerfile` and add required apps. Refer comments in the file.
- Change `worker/Dockerfile` and add required apps.

Example file uses following apps:

- https://github.com/yrestom/POS-Awesome
- https://github.com/zerodha/frappe-attachments-s3
- https://github.com/pipech/frappe-metabase
- https://github.com/franknyarkoh/bookings
- https://github.com/frappe/bench_manager

### Build images

Execute from root of app repo

For nginx:

```shell
# For version-13
docker build --build-arg=FRAPPE_BRANCH=version-13 -t custom-erpnext-nginx:v13 nginx
```

For worker:

```shell
# For version-13
docker build --build-arg=FRAPPE_BRANCH=version-13 -t custom-erpnext-worker:v13 worker
```
