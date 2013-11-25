require './do-credentials.rb'

Vagrant.configure('2') do |config|

  config.vm.provider :digital_ocean do |provider, config|
    config.ssh.private_key_path = DO_CREDENTIALS::PRIVATE_KEY_PATH
    config.ssh.username = DO_CREDENTIALS::USERNAME
    config.vm.box = 'digital_ocean'
    config.vm.box_url = 'https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box'
    config.vm.hostname = 'cross-bones'

    provider.api_key = DO_CREDENTIALS::API_KEY
    provider.client_id = DO_CREDENTIALS::CLIENT_ID

    # Defaults:
    provider.image = 'Ubuntu 12.04.3 x64'
    # provider.region = 'New York 2'
    # provider.size = '512MB'
    # provider.ssh_key_name = 'Vagrant'
    # provider.setup = true
  end
end
