#Vaprobash xdebub screem override

Created an override file for the vaprobash set up so that it sets the xdebug scream value to 0, to help with a laravel install etc.

Once you have downloaded the Vaprobash file and uncommented what you need at the end is the following option:

```bash
####
  # Local Scripts
  # Any local scripts you may want to run post-provisioning.
  # Add these to the same directory as the Vagrantfile.
  ##########
  # config.vm.provision "shell", path: "./local-script.sh"

```

Simply create a file called  local-script., copy and paste the xdebug override code within this file, thenplace within the same folder as the Vaprobash file. 

Then simply uncomment the last line, so you get:

```bash
####
  # Local Scripts
  # Any local scripts you may want to run post-provisioning.
  # Add these to the same directory as the Vagrantfile.
  ##########
  
   config.vm.provision "shell", path: "./local-script.sh"

```

then when you run vagrant up it will run through everythign then run you script last, updating the previous php.sh xdebug setting and basically setting.

```bash
xdebug.scream =0
```

i coudl simply download the scripts file and alter the php.sh file, but then the script fiels will become out of date etc if linked locally. Anyway its  asuggestion.