require './do-credentials.rb'

Vagrant.configure('2') do |config|

  config.vm.provider :digital_ocean do |provider, override|
    override.ssh.username = 'marius'
    override.ssh.private_key_path = DO_CREDENTIALS::PRIVATE_KEY_PATH
    override.vm.box = 'digital_ocean'
    override.vm.box_url = 'https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box'
    override.vm.hostname = 'x-bones'

    provider.client_id = DO_CREDENTIALS::CLIENT_ID
    provider.api_key = DO_CREDENTIALS::API_KEY

    # Defaults:
    # provider.image = 'Ubuntu 12.04 x64'
    # provider.region = 'New York 2'
    # provider.size = '512MB'
    # provider.ssh_key_name = 'Vagrant'
    # provider.setup = true
  end
end
