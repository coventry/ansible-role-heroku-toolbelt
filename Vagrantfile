Vagrant.configure('2') do |config|
  config.vm.define 'ansible-role-heroku-toolbelt' do |c|
    c.vm.box = 'ubuntu/trusty64'
    c.vm.network :private_network, ip: '192.168.40.7'
    c.vm.hostname = 'ansible-role-heroku-toolbelt.local'

    c.vm.provider :virtualbox do |vb|
      vb.name = 'ansible-role-heroku-toolbelt'
    end

    c.vm.provision :ansible do |ansible|
      ansible.playbook = 'test.yml'
      ansible.sudo = true
      ansible.inventory_path = 'vagrant-inventory'
      ansible.host_key_checking = false
      ansible.verbose = 'vvv'
      ansible.extra_vars = {
        heroku_toolbelt_users: %w(root vagrant)
      }
    end
  end
end
