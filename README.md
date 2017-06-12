# Docker LemonSync
Sync local theme files to your Lemon Stand store using the lemonsync command line utility.

## Usage

### Environment Variables
Set the HOST, KEY and ACCESS environment variables.

Opitonally set the IGNORE_PATTERNS and FILE_PATTERNS environment variables.

### Volumes
Mount your local theme directory to /working_dir. Files in this folder will be synced to the remote Lemon Stand store.

## Example docker-compose.yaml

```
version: '2'
services:
  lemonsync:
    image: threevl/lemonsync:latest
    environment:
      HOST: ${HOST}
      KEY: ${KEY}
      ACCESS: ${ACCESS}
      IGNORE_PATTERNS: ${IGNORE_PATTERNS} #optional
      FILE_PATTERNS: ${FILE_PATTERNS} #optional
    volumes:
      - ./working_dir:/working_dir
```

## Additional Information
For more information see the lemonsync repository: [https://github.com/lemonstand/lemonsync](https://github.com/lemonstand/lemonsync)