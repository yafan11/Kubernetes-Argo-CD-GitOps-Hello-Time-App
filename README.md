# 🚀 Kubernetes Argo CD GitOps Hello Time App

![GitHub release](https://img.shields.io/github/release/yafan11/Kubernetes-Argo-CD-GitOps-Hello-Time-App.svg) ![Docker](https://img.shields.io/badge/docker-%20%F0%9F%8C%8D%20%F0%9F%8C%8D%20%F0%9F%8C%8D-blue) ![Kubernetes](https://img.shields.io/badge/kubernetes-%20%F0%9F%9A%80%20%F0%9F%9A%80%20%F0%9F%9A%80-lightblue)

Welcome to the **Kubernetes Argo CD GitOps Hello Time App**! This project showcases a simple, containerized web application that displays the current time. It is deployed to a Kubernetes cluster using Argo CD and follows GitOps best practices.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Releases](#releases)

## Project Overview

The **Hello Time App** is designed to be simple yet effective. It allows users to view the current time in a web interface. This project emphasizes the use of modern deployment techniques, particularly focusing on Kubernetes and Argo CD for continuous delivery.

## Features

- Displays the current time.
- Containerized using Docker.
- Deployed on Kubernetes.
- Managed using Argo CD.
- Follows GitOps best practices for version control and deployment.

## Technologies Used

This project utilizes the following technologies:

- **Kubernetes**: For orchestrating containerized applications.
- **Argo CD**: For continuous delivery and GitOps.
- **Docker**: For containerization.
- **Nginx**: As a web server to serve the static site.
- **Git**: For version control.

## Installation

To set up the Hello Time App on your local machine, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yafan11/Kubernetes-Argo-CD-GitOps-Hello-Time-App.git
   cd Kubernetes-Argo-CD-GitOps-Hello-Time-App
   ```

2. **Build the Docker image**:
   ```bash
   docker build -t hello-time-app .
   ```

3. **Run the Docker container**:
   ```bash
   docker run -d -p 8080:80 hello-time-app
   ```

4. **Access the application**:
   Open your web browser and go to `http://localhost:8080` to see the current time displayed.

## Usage

Once the application is running, you can view the current time in your web browser. The application refreshes automatically to show the updated time. This simple functionality demonstrates how easy it is to deploy a web application using modern tools.

## Deployment

To deploy the Hello Time App to a Kubernetes cluster using Argo CD, follow these steps:

1. **Install Argo CD**:
   You can install Argo CD in your Kubernetes cluster by following the [official installation guide](https://argo-cd.readthedocs.io/en/stable/getting_started/).

2. **Create a new application in Argo CD**:
   Use the following command to create a new application:
   ```bash
   argocd app create hello-time-app --repo https://github.com/yafan11/Kubernetes-Argo-CD-GitOps-Hello-Time-App --path . --dest-server https://kubernetes.default.svc --dest-namespace default
   ```

3. **Sync the application**:
   Sync the application to deploy it:
   ```bash
   argocd app sync hello-time-app
   ```

4. **Access the application**:
   Once deployed, you can access the application through the external IP of your Kubernetes service.

## Contributing

We welcome contributions to improve the Hello Time App. To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or feedback, please reach out to [yafan11](https://github.com/yafan11).

## Releases

You can find the latest releases of the Hello Time App [here](https://github.com/yafan11/Kubernetes-Argo-CD-GitOps-Hello-Time-App/releases). Download the latest version and follow the installation instructions to get started.

---

Thank you for checking out the **Kubernetes Argo CD GitOps Hello Time App**! We hope you find it useful. For any issues or suggestions, please check the "Releases" section or reach out to us directly. Happy coding!