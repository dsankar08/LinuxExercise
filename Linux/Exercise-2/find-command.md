# Problem 

## Do in Linux

- a. On App Server 2 at location /var/www/html/blog  find out all files (not directories) having .js extension.

- b. Copy all those files along with their parent directory structure to location /blog on same server.

- c. Please make sure not to copy the entire /var/www/html/blog  directory content.


## Solution

- `cd /var/www/html/blog`
- `find . -type f -name "*.js" -exec cp --parents {} /blog \;`
