# Jenkins Repository

This repository contains example Jenkins pipelines, helper scripts, and a small MiniProject that demonstrates building and deploying a containerized app.

## Contents

- `Jenkinsfile`, `Jenkinsfile_v1`, `Jenkinsfile_v2` - pipeline examples in the repository root.
- `MiniProject/` - a small example project containing a `Dockerfile`, `deploy.yml`, `inventory`, and its own Jenkinsfiles.
- Shell scripts and small programs: `c.sh`, `mul.sh`, `calculator.sh`, `a.c`, `HelloWorld.py`, `Prog1.py`, `Test.py`.

## Purpose

Provide sample Jenkins pipeline configurations and an example project you can use to learn Jenkins pipeline creation, Docker builds, and simple CI/CD flows.

## Prerequisites

- Jenkins (recommended 2.x with Pipeline plugin)
- Docker (to build and run the MiniProject container)
- Git
- Python 3 (for the example scripts)

## Quick Start

1. Clone the repository:

```
git clone <repository-url>
cd Jenkins-master
```

2. Run an example Python script:

```
python3 HelloWorld.py
```

3. Run shell scripts:

```
sh c.sh
sh mul.sh
```

4. Use a Jenkinsfile in Jenkins:

- Create a new Pipeline job in Jenkins and point it to this repository (SCM). Choose the `Jenkinsfile` you want to run (root or MiniProject/Jenkinsfile).

5. Build and run the MiniProject Docker image (optional):

```
cd MiniProject
docker build -t miniapp .
docker run -d -p 8080:80 miniapp
```

Note: Adjust ports or image name as required by the `MiniProject/Dockerfile`.

## Project Layout (high level)

- Root Jenkinsfiles: pipeline examples for different versions/approaches.
- `MiniProject/`: example app, Dockerfile, Ansible inventory (`inventory`) and deployment manifest (`deploy.yml`).
- Misc scripts and example programs in the repository root.

## Contributing

Feel free to open issues or submit pull requests to improve pipeline examples and documentation.

## License

This repository does not include a license file. Add one if you plan to publish or share widely.

## Contact

Repository owner: Shikhar Mutta 
Email: shikharmutta67@gmail.com
