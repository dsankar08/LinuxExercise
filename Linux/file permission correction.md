# First problem 

## Do in Linux

 The file named /etc/hostname on Nautilus App 1 server requires adjustments to its Access Control Lists

- 1. The file's user owner and group owner should be set to root.

- 2. Others should possess read only permissions on the file.

- 3. User rose must not have any permissions on the file.

- 4. User eric should be granted read only permission on the file.

## Solution

we have to use `getfacl` and `setfacl` here as it is permission is user specific 

`getfacl hostname`

``` # file: hostname
# owner: root
# group: root
user::rw-
group::r--
other::r--
 ```

`setfacl -m u:eric:r hostname`
`setfacl -m u:rose:- hostname`


## More of Setfacl and getfacl

Use the setfacl command with the -m (modify) option to add an ACL entry for the specified user with read-only permissions.
For a file:
Code

        setfacl -m u:username:r- file.txt
Replace username with the actual username and file.txt with the target file. The r- signifies read-only access. For a directory.
Code

        setfacl -m u:username:rx directory/
Replace username with the actual username and directory/ with the target directory. For directories, you typically grant rx (read and execute/search) permissions so the user can list its contents and traverse into subdirectories.
For a directory and its future contents (default ACL):
Code

        setfacl -m u:username:rx,d:u:username:r directory/
This command grants rx permissions to the user on the directory itself and sets a default ACL (d:u:username:r) so that any new files created within that directory will automatically inherit read-only permissions for that user.
Verify Permissions: Use the getfacl command to verify that the ACL has been applied correctly.
Code

    getfacl file.txt



