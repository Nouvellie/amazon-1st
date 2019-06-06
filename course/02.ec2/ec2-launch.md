# EC2 LAUNCH
## Create

Click on *services* and then **launch**.

- Configure instance:
	- Number of instances: 1. (by default)
	- [ ] Request Spot instances.
	- Network: default vpc.
	- Subnet: any.
	- Auto-assign public IP: Enable.
	- [ ] Placement group. (high performance computing)
	- Capacity reservation: Open.
	- IAM role: None.
	- Shutdown behavior: Stop.
	- [x] Enable termination protection.
	- [ ] Monitoring.
	- Tenancy: Shared.
	- [ ] Elastic interference.
	- [ ] T2/T3 unlimited.
- Add storage:
	- Volume Type: General purpose SSD. (gp2)
	- Size: 8 (GiB)
	- [x] Delete on termination.
- Tags:

| Name  | WebServer |
| --- | --- |
| Department | Developer |