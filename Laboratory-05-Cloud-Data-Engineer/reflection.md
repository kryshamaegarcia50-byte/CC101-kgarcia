# Mission Reflection

This mission helped me understand how object storage works and how it can be used to store many files such as photos. Object storage is better suited for storing millions of photos than traditional block storage because it is designed for large amounts of unstructured data. Each photo can be stored as an object with its own unique identifier and metadata. Object storage can also scale easily when the number of photos continues to increase.

Using Docker made deploying the MinIO storage server easier because I did not need to manually install and configure every component. Docker allowed me to run MinIO inside a container with the required ports and environment variables. This made the deployment process faster and more organized. I also learned that containers make applications easier to move and run in different environments.

A bucket is a storage container used to organize and store objects in object storage. In this mission, I created a bucket named `client-photos` and uploaded a sample file into it. This helped me understand how files are managed in an object storage system.

Large enterprise companies can protect their object storage data from physical server failures by keeping multiple copies of data and using redundancy. They can also store copies across different servers, storage devices, or even different locations. Backups and replication help make sure that data can still be recovered when hardware fails.

My confidence in using the Linux command line is also improving. At first, commands such as navigating directories, creating files, running Docker commands, and checking containers felt difficult. After completing the mission, I became more comfortable using commands like `cd`, `ls`, `docker ps`, `git add`, and `git push`. I still need more practice, but I now feel more confident working with Linux through the command line.
