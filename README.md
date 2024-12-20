# Microfrontend Architecture

This project demonstrates a **Microfrontend (MFE)** architecture using Angular and module federation. The setup allows multiple independently developed applications to integrate seamlessly into a unified experience. Inspired by [Transforming Your Application into Microfrontends with Native Federation](https://medium.com/@erick.98zanetti.98/transforming-your-application-into-micro-frontends-with-native-federation-for-angular-part-1-791d159b09c8), this repository comprises:

- **Shell**: The host application coordinating microfrontends.
- **MFE1**: A standalone feature/module integrated into the Shell.
- **MFE2**: Another standalone feature/module integrated into the Shell.

---

## Prerequisites

Ensure the following tools are installed:

- **Node.js** (v14 or higher)
- **npm** (v6 or higher)

---

## Installation

Install the dependencies for all applications:

```bash
npm --prefix shell i
```

```bash
npm --prefix mfe1 i
```

```bash
npm --prefix mfe2 i
```

---

## Running the Applications

To run the individual applications:

- **Shell**:  
  Starts the host application on `http://localhost:4200`.  
  ```bash
  npm --prefix shell run start
  ```

- **MFE1**:  
  Starts Microfrontend 1 on its own server.  
  ```bash
  npm --prefix mfe1 run start
  ```

- **MFE2**:  
  Starts Microfrontend 2 on its own server.  
  ```bash
  npm --prefix mfe2 run start
  ```

### Run All Applications Simultaneously

You can run all applications concurrently with the following commands:

### For Linux or macOS:

```bash
npm --prefix shell run start & npm --prefix mfe1 run start & npm --prefix mfe2 run start
```

### For Windows:

```bash
npm --prefix shell run start && npm --prefix mfe1 run start && npm --prefix mfe2 run start
```

Now you can easily copy and paste the appropriate command for your operating system.


---

## Accessing the Applications

- **Shell**: Open `http://localhost:4200` in your browser to view the integrated application.
- **MFE1** and **MFE2**: Dynamically load into the Shell based on navigation or configuration.

Each microfrontend can also be accessed independently during development by visiting their respective local URLs.

---

## Example Workflow

1. Start all applications using the above commands.
2. Open the **Shell** application in your browser.
3. Make changes to any microfrontend or the Shell, and the changes will reflect in real time during development.

---

## Further Reading

For more details on module federation and microfrontends in Angular, refer to the article [Transforming Your Application into Microfrontends with Native Federation](https://medium.com/@erick.98zanetti.98/transforming-your-application-into-micro-frontends-with-native-federation-for-angular-part-1-791d159b09c8).

