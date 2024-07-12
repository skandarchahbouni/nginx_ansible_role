# Setting up git  
    - git config --global user.email "js_chahbouni@esi.dz"
    - git config --global user.name "Skandar-Ramzi CHAHBOUNI"

# Installing ansible 
    - sudo apt update
    - sudo apt install pipx
    - pipx ensurepath
    - pipx install --include-deps ansible
    - pipx install ansible-core
    - pipx upgrade --include-injected ansible
    - pipx inject ansible argcomplete
    - pipx inject --include-apps ansible argcomplete

# Setting up ssh
    - change the ip address in the inventory 
    - ssh-keygen -t ed25519 -C "ansible"
    - copy the public key to the managed node 
    - ssh -i ../.ssh/ansible <IP_Address>
    - check that you are good to go: ansible all -m ping


# Testing Installation
    - which nginx
    - systmectl nginx 
    - curl http://localhost