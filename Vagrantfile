ENV['VAGRANT_DEFAULT_PROVIDER'] = 'libvirt'
IMAGEN = "generic/ubuntu2004"

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", type: "rsync",  disabled: true

  config.vm.define "ftp" do |f|
    f.vm.box = IMAGEN
    f.vm.hostname = "ftp"
    f.vm.box_check_update = false

    f.vm.provider :libvirt do |v|
      v.memory = 1024
      v.cpus = 2
    end
  end
end



