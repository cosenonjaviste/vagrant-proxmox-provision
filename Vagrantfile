Vagrant.configure('2') do |config|
	config.vm.provider :proxmox do |proxmox|
		proxmox.endpoint = 'https://192.168.202.135:8006/api2/json'
		proxmox.user_name = 'root@pam'
		proxmox.password = '221172u'
		proxmox.os_template = '/var/lib/vz/template/cache/vagrant-proxmox-ubuntu-12.tar.gz'
		proxmox.vm_id_range = 101..101
		proxmox.vm_name_prefix = 'vagrant_test_'
		proxmox.vm_memory = 512
		proxmox.task_timeout = 30
		proxmox.task_status_check_interval = 1
	end

	config.vm.define :box, primary: true do |box|
		box.vm.box = 'dummy'
	end
end
