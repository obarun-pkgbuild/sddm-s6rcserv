# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=sddm-s6rcserv
pkgver=0.1
pkgrel=2
pkgdesc="sddm service for s6"
arch=(x86_64)
license=('beerware')
depends=('sddm' 's6' 's6-rc' 's6-boot')
conflicts=()
install=sddm-s6rcserv.install
source=('sddm.daemon.dependencies.s6'
		'sddm.daemon.finish.s6'
		'sddm.daemon.pipeline-name.s6'
		'sddm.daemon.producer-for.s6'
		'sddm.daemon.run.s6'		
		'sddm.daemon.type.s6'	
		
		'sddm.log.consumer-for.s6'
		'sddm.log.dependencies.s6'
		'sddm.log.run.s6'
		'sddm.log.type.s6'
		
		'bundle.sddm.contents.s6'
		'bundle.sddm.type.s6'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '46a3812ba654b86bae132fca8d002c83'
         '657659d0a59287daf0f0ed7095e5de72'
         '782e77a03a4760d9b4101fa707e97405'
         'e9222e0a3f62e1fca2173e22d756650f'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '0fb01ed2f4246300aeb7cb8a719752a0'
         '68b329da9893e34099c7d8ad5cb9c940'
         '5fbe0a85ff8b8774ed9d76eec10fba7a'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '9d6df462fa6ec2589e95f482d898be8b'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-sddm need a maj at sddm e.g user-Base
	install -Dm 0644 "$srcdir/bundle.sddm.contents.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Sddm/contents"
	install -Dm 0644 "$srcdir/bundle.sddm.type.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Sddm/type"
	
	# daemon
	install -Dm 0644 "$srcdir/sddm.daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/sddm-daemon/dependencies"
	install -Dm 0644 "$srcdir/sddm.daemon.finish.s6" "$pkgdir/etc/s6-serv/available/rc/sddm-daemon/finish"
	install -Dm 0644 "$srcdir/sddm.daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/sddm-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/sddm.daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/sddm-daemon/producer-for"
	install -Dm 0644 "$srcdir/sddm.daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/sddm-daemon/run"
	install -Dm 0644 "$srcdir/sddm.daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/sddm-daemon/type"
	
	# log
	install -Dm 0644 "$srcdir/sddm.log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/sddm-log/consumer-for"
	install -Dm 0644 "$srcdir/sddm.log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/sddm-log/dependencies"
	install -Dm 0644 "$srcdir/sddm.log.run.s6" "$pkgdir/etc/s6-serv/available/rc/sddm-log/run"
	install -Dm 0644 "$srcdir/sddm.log.type.s6" "$pkgdir/etc/s6-serv/available/rc/sddm-log/type"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/sddm-s6rcserv/LICENSE"
}
