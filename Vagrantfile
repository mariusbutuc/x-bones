require './do-credentials.rb'

Vagrant.configure('2') do |config|
  config.vm.hostname = 'cross-bones'
  config.vm.provider :digital_ocean do |provider, override|
    override.ssh.private_key_path = DO_CREDENTIALS::PRIVATE_KEY_PATH
    override.ssh.username = DO_CREDENTIALS::USERNAME
    override.vm.box = 'digital_ocean'
    override.vm.box_url = 'https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box'

    provider.api_key = DO_CREDENTIALS::API_KEY
    provider.client_id = DO_CREDENTIALS::CLIENT_ID
    provider.ssh_key_name = DO_CREDENTIALS::USERNAME
    provider.image = 'Ubuntu 12.04.3 x64'
    provider.size = '512MB'                                 # explicit default
    provider.region = 'New York 2'                          # explicit default
  end

  config.omnibus.chef_version = '11.6.0'
end
