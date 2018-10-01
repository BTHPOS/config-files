# Bithereum Configuration

The Bithereum config file is used when running `bethd` (Bithereum daemon) and is located in `~/.bithereum/` directory by default. If you do not have a `~/.bithereum`  directory, please create one. You can check to see if you have this directory by typing in `ls -al`. To create one, type in `mkdir ~/.bithereum`.


## Added config file

With the `~/.bithereum/` directory present, clone this repo to your home directory.
```shell
git clone https://github.com/BTHPOS/config-files.git
```

Copy the config file that you wish to use into the `~/.bithereum/` directory.

```shell
 cp ~/config-files/BTH/bithereum_conf/testnet.conf ~/.bithereum/bithereum.conf
```

## Test configuration

Run the bithereum daemon to test your configuration file
```shell
./bethd
```

## Verifying that your configuration are working

To verify that your configurations are working, open up the bithereum.conf file
```shell
vim ~/.bithereum/bithereum.conf
```

Change `daemon=1` to `daemon=0` and then save the file.
```conf
daemon=0    # Runs this process in the background
```

Now run the daemon with the print to console command to read the run log
```shell
./bethd -printtoconsole
```
