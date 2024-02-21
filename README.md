# Data Version Control with DVC

## Initialization

### Initialize Git and DVC:

- `git init`: Initializes a new Git repository.
- `dvc init --subdir`: Initializes a new DVC repository in a subdirectory called ".dvc".

### Commit Initializations:

- `git status`: Checks which files are untracked or modified.
- `git commit -m "DVC initialized"`: Commits the DVC initialization.

## Remote Storage Setup

### Add Remote Storage:

- `dvc remote add -d remote_storage gdrive://1qmHWUWrdxtVzVNPsztMlrmmRHSaVnheb -f`: Adds remote storage using Google Drive.

### Commit Remote Storage Addition:

- `git add .dvc/config`: Adds the DVC configuration changes.
- `git commit -m "Updated remote storage"`: Commits the addition of remote storage.

## Data Preparation and Versioning

### Save Raw Data

- Save pre-processed raw data to a CSV file.
- Split the data into train, test, and validation sets.
- Add these 3 files to DVC.
- Add DVC metadata files of the above 3 to Git.
- Push these files using DVC.

### Versioning

- Repeat the above steps for different seeds.
- Check Git log for commit history.
- Use `git checkout` to checkout specific files from a specific commit.
- Use `dvc checkout` to restore datasets to their state at a specific commit or branch.

### Analyze Data

- Save the files and analyze the distribution of data.
- This approach allows tracking of all updates and changes made to the data.
