# SSH

Project exploring SSH fundamentals: key-pair authentication, client configuration, and secure remote access to a cloud server.

## Tasks

### 0. Use a private key
`0-use_a_private_key` — Connects to the server using private key `~/.ssh/school` with user `ubuntu`.

### 1. Create an SSH key pair
`1-create_ssh_key_pair` — Generates a 4096-bit RSA key pair named `school`, passphrase `betty`.

### 2. Client configuration file
`2-ssh_config` — SSH client config enforcing key-based auth, no passwords.

### 3. Let me in!
Added the ALU public key to the server's `~/.ssh/authorized_keys`.
