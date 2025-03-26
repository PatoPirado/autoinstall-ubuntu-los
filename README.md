# Galactic Ubuntu Auto Install
## Usage

1. Download the official Ubuntu ISO.
2. Extract it to a folder of your preference.
3. Place the `autoinstall.yaml` file into the root of the extracted Ubuntu folder.
4. Create the custom ISO using the following command:

    ```bash
    xorriso -as mkisofs -r -V "Name of the Image" -o ../losubuntu.iso -J -l -b boot/grub/i386-pc/eltorito.img -c boot.catalog -no-emul-boot -boot-load-size 4 -boot-info-table folder-with-the-ubuntus-iso-files/
    ```

5. Ensure `xorriso` and `mkisofs` are installed on your system.

## Finding the Custom ISO

The custom ISO will be located in the parent directory of your working folder unless specified otherwise.
