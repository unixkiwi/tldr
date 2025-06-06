# sha384sum

> Calculate SHA384 cryptographic checksums.
> More information: <https://www.gnu.org/software/coreutils/manual/html_node/sha2-utilities.html>.

- Calculate the SHA384 checksum for one or more files:

`sha384sum {{path/to/file1 path/to/file2 ...}}`

- Calculate and save the list of SHA384 checksums to a file:

`sha384sum {{path/to/file1 path/to/file2 ...}} > {{path/to/file.sha384}}`

- Calculate a SHA384 checksum from `stdin`:

`{{command}} | sha384sum`

- Read a file of SHA384 checksums and filenames and verify all files have matching checksums:

`sha384sum {{[-c|--check]}} {{path/to/file.sha384}}`

- Only show a message for missing files or when verification fails:

`sha384sum {{[-c|--check]}} --quiet {{path/to/file.sha384}}`

- Only show a message when verification fails, ignoring missing files:

`sha384sum --ignore-missing {{[-c|--check]}} --quiet {{path/to/file.sha384}}`

- Check a known SHA384 checksum of a file:

`echo {{known_sha384_checksum_of_the_file}} {{path/to/file}} | sha384sum {{[-c|--check]}}`
