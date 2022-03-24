# Folder Scavenger

Walks folder structure, deleting files by age to maintain % of free folder space.

## Environment Variables

| Name                     | Description                                                                           | Default |
|--------------------------|---------------------------------------------------------------------------------------|---------|
| DEBUG                    | If 'True', debug logging is used. Else info                                           | True    |
| SLEEP_SECONDS            | How long to sleep for between iterations                                              | 1       |
| ROOT_FOLDER              | Entrypoint for scavenging                                                             |         |
| MINIMUM_AGE              | Minimum age, in secs, for folder to be considered for deletion                        | 0       |
| DELETE_LEAF_CONTENTS     | If `True`, will attempt to delete individual leaf files                               | False   |
| FREE_SPACE_THRESHOLD     | % of freespace beyond which scavenging will take place                                | 100     |
| USE_INODES               | If `True`, [inodes](https://en.wikipedia.org/wiki/Inode) used to check free spaces    | False   |
| CHECK_FILE_AGE           | If `True`, file age is checked prior to deleting                                      | False   |
| SLACK_WEBHOOK_URL        | Optional URL to announce to                                                           | `None`  |
| WAIT_FOR_ROOT_TO_EXIST   | If `True`, process will wait for `ROOT_FOLDER` to exist. If `False` assumes it exists | False   |
| PROCESS_INDIVIDUAL_FILES | If `True`, individual files are checked. If `False` only folders checks               | False   |