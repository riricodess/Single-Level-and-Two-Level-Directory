# File Organization Schemes: Single-Level and Two-Level Directory

## Aim
To implement single-level and two-level directory organization schemes and compare their worst-case file-name lookup comparisons.

## Programs
- `dir.c` — Single-Level Directory
- `dir2.c` — Two-Level Directory

## Requirements
- GCC compiler
- Linux, macOS, or Windows with GCC installed

## Program 1: Single-Level Directory

### Compile and Run
```bash
gcc dir.c -o dir
./dir
```

### Expected Output
```text
Server: 4 users x 250 files each
Total files: 1000
Single level worst case: 1000 comparisons
```

## Program 2: Two-Level Directory

### Compile and Run
```bash
gcc dir2.c -o dir2
./dir2
```

### Expected Output
```text
Server: 4 users x 250 files each
Two level worst case: 254 comparisons
```

## Explanation

### Single-Level Directory
In a single-level directory, all users store their files in one common directory. With four users storing 250 files each, the total number of files is 1,000. In the worst case, the system may need to compare all 1,000 file entries.

### Two-Level Directory
In a two-level directory, each user has a separate directory. The system first searches for the user's directory and then searches for the requested file inside it. Based on the experiment's calculation, the worst-case comparisons are:

`4 + 250 = 254 comparisons`

This structure also allows different users to store files with the same name in their own directories.

## Conclusion
The experiment demonstrates the difference between single-level and two-level directory organization. In this example, the two-level directory requires fewer file-name comparisons and reduces naming conflicts between users.
