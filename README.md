# Strongloop Test Application

The project is generated by [LoopBack](http://loopback.io).

### Requirement

- You need to have [Vagrant](https://www.vagrantup.com/)

- You need to have [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

### Note

- This particular project is using one of the publicly available Vargrant Boxes which is [node-trusty](https://atlas.hashicorp.com/strongloop/boxes/node-trusty).

### Installation

1. Clone the repo.
    ```sh
    $ git clone https://github.com/meolinden/alpha-loopback.git && cd alpha-loopback
    ```

2. Update the values of vagrant.yml. These values will be used to to setup vm. While you can choose any local ip address you'd like, you should use an IP from the [reserved private address space](https://en.wikipedia.org/wiki/Private_network#Private_IPv4_address_spaces). 

3. Update your host file (/etc/hosts) 

4. Boot up the local server
    ```sh
    $ vagrant up --provider virtualbox
    ```
    or 
    ```sh
    $ vagrant up
    ```
    since the default provider is virtualbox
5. Access the vm.
    ```sh
    $ vagrant ssh
    ```
6. Go to the project folder you defined on vagrant.yml `folder` 
    ```sh
    $ cd /var/www/project-folder
    ```

7. Execute `slc run`. 

8. Access the app on you browser using the domain you provided in config.yml. `eg. http://[domain]:3000/explorer`

### For Existing Strongloop/loopback projets

1. Go to https://github.com/meolinden/alpha-loopback

2. Add the vagrantfile and vagrant.yml on your existing repository

3. Update the values on vagrant.yml accordingly.

4. Boot up the local server
    ```sh
    $ vagrant up --provider virtualbox
    ```
    or 
    ```sh
    $ vagrant up
    ```
    since the default provider is virtualbox

5. Access the vm.
    ```sh
    $ vagrant ssh
    ```

6. Go to the project folder you defined on vagrant.yml `folder` 
    ```sh
    $ cd /var/www/project-folder
    ```

7. Execute `slc run`.

8. Access the app on you browser using the domain you provided in config.yml. `eg. http://domain:3000/explorer`


### TIPS 
1. Use `vagrant reload` to restart your server

