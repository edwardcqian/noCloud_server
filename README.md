# noCloud Server
Setup a semi-production grade linux cluster for local file sharing, project development, and project hosting.

## Overview
Components includes:
- samba for local file sharing
- openssh for accessing local network
- kubernetes and docker for hosting services (upcoming)
- airflow for task orchestration (upcoming)

## What can you do with this server?
- do development at home
- remote access your home cluster
- host simple application for free (freeish, you still need to pay for electricity)
- schedule periodic tasks
- share file at home via network drive

## Important vs Nice to have
- openssh (important): if you do remote dev, this is the best way
- docker (important): trying to make things consistent across different platform/machines is a headache
- samba (nice to have): local file sharing is nice, but not exactly required for development
- kubernetes (nice to have): quite extensive, might be too much work for just a hobby server
- airflow (nice to have): a powerful tool if you want to schedule an automate tasks