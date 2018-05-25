Vagrant.configure '2' do |c|
  c.vm.define 'alice' do |a|
    a.vm.box = 'bento/ubuntu-16.04'
    a.vm.hostname = 'alice'
    a.vm.network 'private_network', ip: '192.168.0.2'
  end

  c.vm.define 'bob' do |b|
    b.vm.box = 'bento/ubuntu-16.04'
    b.vm.hostname = 'bob'
    b.vm.network 'private_network', ip: '192.168.0.3'
  end
end