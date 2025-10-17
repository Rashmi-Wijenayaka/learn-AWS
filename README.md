# learn-AWS

### AWS fragate is a new technology for managing containers. ELB not supporting with fargate.
### Container Security Risks: Segregation (Confidentiallity) - Container to Container, Process to Process, Container to Outside
### Access(Who/When/Where, Logging, Start/Stop, Content) and Resource usage are affect for Container security.
### The system is included with:
<img width="1247" height="706" alt="image" src="https://github.com/user-attachments/assets/ee79531c-09f8-4827-a8c4-95252fb21bc6" />

### The all applications ARE SITTING ON THE same kernel. They use same syscall interface. They use same cpu scheduler and memory scheduler. They use same underneath the platform. They use huge demand of shared resources. It's generating some risks. Subsystems of the kernel have additional functions. To ptovide isolazion, segmentation and management of those containers.
### Functionallity called as namespaces. ( PID-Namespace, CPU/Memory-Namespace (cgroup), Network-Namespace, User-Namespace, FS/Mount-Namespace )
### IPC-Namespace(Taking care of Inter Process Comunication)

<img width="782" height="456" alt="Screenshot 2025-10-17 201647" src="https://github.com/user-attachments/assets/fec2b7f1-e2ba-48d5-8946-4d407fecffa7" />

### Different namespaces for sametime. They can share namespace of different type. They seem both same network connectivity. See each other process information. They see both same network connectivity.
### PID Namespace has 2 PIDs. Global PID for global namespcae and local PID for local area. Inside only see local space and in the kernel we can see both namespaces. Processes of namespaces can't see each other. 1st namespace get local PID 0. We can move on namespaces. All lift on the same memory management. Memory fragmentation can happen. We worked in unified shared memory. We get into the namespace with syscall clone. 
