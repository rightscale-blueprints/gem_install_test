Vagrant::Config.run do |config|

  # name of vagrant box
  config.vm.box = "gem_install_test"

  # chef-solo provisioning
  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = 'cookbooks'
    chef.json.merge!(JSON.parse(File.read('node.json')))
    chef.run_list = JSON.parse(File.read('node.json'))['run_list']
    #chef.run_list = []
    #chef.log_level = :debug
  end

end