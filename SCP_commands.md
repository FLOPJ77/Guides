
# SCP Cheat Sheet

A quick reference for copying files and directories over SSH.

**Basic Syntax:**
```bash
scp [options] source destination
```
```bash
scp file.txt user@remote_host:/path/to/destination/
```
```bash
scp user@remote_host:/path/to/file.txt /local/destination/
```
```bash
scp -r user@remote_host:/path/to/folder /local/destination/

```

# SCP Quick Reference

**Syntax:** `scp [options] <source> <destination>`

| Action | Direction | Command |
| :--- | :---: | :--- |
| **Upload file** | Local ➔ Remote | `scp file.txt user@remote_host:/path/to/destination/` |
| **Upload directory** | Local ➔ Remote | `scp -r /local/folder user@remote_host:/path/to/destination/` |
| **Download file** | Remote ➔ Local | `scp user@remote_host:/path/to/file.txt /local/destination/` |
| **Download directory** | Remote ➔ Local | `scp -r user@remote_host:/path/to/folder /local/destination/` |
| **Custom port** | — | `scp -P 2222 file.txt user@remote_host:/path/` |
| **Use SSH key** | — | `scp -i ~/.ssh/id_rsa file.txt user@remote_host:/path/` |
| **Enable compression** | — | `scp -C file.txt user@remote_host:/path/` |
| **Preserve timestamps & permissions** | — | `scp -p file.txt user@remote_host:/path/` |
| **Full combination** | Local ➔ Remote | `scp -i ~/.ssh/id_rsa -P 2222 -r /folder user@remote_host:/path/` |

```bash
scp -i ~/.ssh/my_key.pem -P 2222 -r ./my-folder user@remote_host:/var/www/
```
