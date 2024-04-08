# Training - Stegano I

This challenge give you one photo, and the title already talk about everything, this mean the photo MUST hidden some information in it.

## Tip

This photo have some information in it.

## Solution

1. We can just double click to open it, it look so weird.

1. In Linux environment we can use ``file`` command to check what type of file is.

    ![file_command](<Training-Stegano I_file_command.png>)

1. Then we find it "PC bitmap", let check some information about it. [Here](https://en.wikipedia.org/wiki/BMP_file_format)

1. Now we know about it may be can hidden some information in it. We can just ``cat`` it.

    ![cat_file](<Training-Stegano I_cat_file.png>)

1. We can see passwd, but have some weird text, and we can use ``hexyl`` to check it binary file.

    ![hexyl](<Training-Stegano I_hexyl.png>)

## Additional Task

1. Can explain under message?

    ```binary
    42 4d 66 00 00 00 00 00 00 00 36 00 00 00
    ```

    [ANSWER](https://en.wikipedia.org/wiki/BMP_file_format#Bitmap_file_header)

## References

* https://en.wikipedia.org/wiki/BMP_file_format

* https://www.geeksforgeeks.org/top-10-hex-editors-for-linux/
