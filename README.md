# 🚀 AWS EBS Snapshot & Disaster Recovery on Amazon EC2

A hands-on AWS Cloud project demonstrating how to create Amazon EBS volumes, take point-in-time snapshots, restore volumes from snapshots, and verify data integrity using Ubuntu Linux on Amazon EC2.

---

# 📌 Project Overview

This project simulates a real-world disaster recovery scenario using Amazon EC2 and Amazon EBS.

In this lab, I learned how to:

- Create and attach an Amazon EBS volume
- Format and mount an EBS volume on Linux
- Store application data
- Create a point-in-time EBS Snapshot
- Restore a new EBS volume from the snapshot
- Mount the restored volume
- Verify successful data recovery
- Demonstrate volume independence
- Clean up AWS resources following best practices

---

# 🛠️ Tech Stack

| Service | Description |
|---------|-------------|
| Amazon EC2 | Ubuntu Server |
| Amazon EBS | Persistent Block Storage |
| Amazon EBS Snapshots | Backup & Disaster Recovery |
| Ubuntu Linux | Operating System |
| Bash CLI | Linux Administration |
| Region | ap-south-1 (Mumbai) |

---

# ⚡ Implementation Steps

## Step 1 — Create an Amazon EBS Volume

- Created a new **3 GiB gp3 EBS Volume**
- Attached it to the EC2 instance
- Formatted it with the **ext4** filesystem
- Mounted it at:

```text
/mnt/mydata
```

- Created sample files for testing.

---

## Step 2 — Create an EBS Snapshot

Created a point-in-time snapshot of the EBS volume.

Snapshot Name:

```text
mydata backup
```

---

## Step 3 — Restore from Snapshot

Created a brand-new **3 GiB gp3 EBS Volume** using the snapshot.

Attached the restored volume to the EC2 instance.

Mounted it at:

```text
/mnt/restored_data
```

---

## Step 4 — Verify Data Recovery

Verified that all files were successfully restored.

Created a new file inside the restored volume:

```text
new_backup_file.txt
```

Confirmed that:

- Original volume remained unchanged.
- Restored volume worked independently.

---

# 🐧 Linux Commands Used

```bash
lsblk
fdisk -l
mkfs.ext4
mkdir
mount
umount
df -h
grep -E
touch
ls -l
```

---

# 📸 Project Screenshots

### 1. AWS EBS Volumes Overview

![AWS Volumes](images/AWS_Console_EBS_Volumes_List.png)

---

### 2. AWS Snapshot Overview

![AWS Snapshots](images/AWS_Console_Snapshots_List.png)

---

### 3. Snapshot Restoration Verification

![Terminal Verification](images/AWS_EBS_Snapshot_Restoration_Proof.png)

---

# 🎯 Learning Outcomes

Through this project, I learned:

- Amazon EBS architecture
- Persistent storage in AWS
- EBS Volume attachment
- Linux filesystem formatting
- Mounting and unmounting disks
- Point-in-time EBS Snapshots
- Snapshot restoration
- Data integrity verification
- Disaster recovery workflow
- Linux storage management

---

# 🧹 Resource Cleanup

To minimize AWS costs:

- Unmounted the restored volume
- Detached the restored EBS volume
- Deleted the restored EBS volume
- Deleted unnecessary snapshots after verification

---

# 📚 AWS Services Covered

- Amazon EC2
- Amazon EBS
- Amazon EBS Snapshots

---

# 👨‍💻 Author

**Pavan Kushwaha**

AWS Cloud Engineer Learning Journey
