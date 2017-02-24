*Commonly used tests:*

    -d FILE
          FILE exists and is a directory
    -e FILE
          FILE exists
    -f FILE
          FILE exists and is a regular file
    -h FILE
          FILE exists and is a symbolic link (same as -L)
    -r FILE
          FILE exists and is readable
    -s FILE
          FILE exists and has a size greater than zero
    -w FILE
          FILE exists and is writable
    -x FILE
          FILE exists and is executable
    -z STRING
          the length of STRING is zero
          
*Example:*

    if [ -e "$file_name" ] && [ ! -z "$used_var" ]
    then
        echo "$file_name exists and $used_var is not empty"
    fi
