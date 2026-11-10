
# Capacity Estimation
## Photo Intelligence Platform

### 1. Initial Assumptions

| Parameter | Value |
|---|---:|
| Registered Users | 10,000 |
| Daily Active Users | 2,000 |
| Photos per User per Day | 10 |
| Average Photo Size | 5 MB |
| Maximum Photo Size | 20 MB |
| Maximum Batch Size | 100 |

These are provisional learning assumptions.

### 2. Daily Upload Calculation

Daily Uploads = DAU × Photos per User

= 2,000 × 10

= 20,000 photos/day

### 3. Storage Estimation

Daily Storage = Daily Uploads × Average Photo Size

= 20,000 × 5 MB

= 100 GB/day

Monthly Storage = 100 GB × 30

= 3 TB/month

Yearly Storage = 100 GB × 365

= 36.5 TB/year

### 4. Average Upload Rate

Seconds per day = 86,400

Average Photo Upload Rate = 20,000 / 86,400

= 0.23 photos/second

### 5. Peak Upload Rate

Assumed Peak Multiplier = 10

Peak Upload Rate = 0.23 × 10

= 2.3 photos/second

This is an illustrative assumption and needs validation.

### 6. Bandwidth Estimation

Average Incoming Data = 100 GB/day

Average Incoming Bandwidth ≈ 1.16 MB/second

Illustrative Peak Bandwidth ≈ 11.6 MB/second

### 7. Storage Architecture Decision

- Azure Blob Storage stores original photos.
- PostgreSQL stores photo metadata.
- Backend manages upload authorization and photo records.
- Future processing workers generate thumbnails and AI metadata.

### 8. Limitations

- Does not include thumbnail storage.
- Does not include backups or replication.
- Does not include photo downloads.
- Does not include AI processing workload.
- Peak multiplier is an assumption, not production traffic data.

