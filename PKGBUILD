# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=sddm-s6rcserv
pkgver=0.1
pkgrel=3
pkgdesc="sddm service for"
arch=(x86_64)
license=('beerware')
depends=('sddm' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('sddm.longrun.dependencies'
		'sddm.longrun.finish'
		'sddm.longrun.pipeline-name'
		'sddm.longrun.producer-for'
		'sddm.longrun.run'		
		'sddm.longrun.type'	
		
		'sddm.log.consumer-for'
		'sddm.log.dependencies'
		'sddm.log.run'
		'sddm.log.type'
		
		'bundle.sddm.contents'
		'bundle.sddm.type'
		'sddm.logd'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '46a3812ba654b86bae132fca8d002c83'
         '657659d0a59287daf0f0ed7095e5de72'
         '782e77a03a4760d9b4101fa707e97405'
         'e9222e0a3f62e1fca2173e22d756650f'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '112ac49da4d94dc1bc232bf61fb741d3'
         '68b329da9893e34099c7d8ad5cb9c940'
         '5fbe0a85ff8b8774ed9d76eec10fba7a'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'a2646158690dbbd8359051b3d0bbdd3c'
         '71abe97e2554d37f1d12c5bf4945297f'
         '9c55376633771d722d97c7b60b841988'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-sddm need a maj at sddm e.g user-Base
	install -Dm 0644 "$srcdir/bundle.sddm.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Sddm/contents"
	install -Dm 0644 "$srcdir/bundle.sddm.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Sddm/type"
	
	# longrun
	install -Dm 0644 "$srcdir/sddm.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/sddm-longrun/dependencies"
	install -Dm 0644 "$srcdir/sddm.longrun.finish" "$pkgdir/etc/s6-serv/available/rc/sddm-longrun/finish"
	install -Dm 0644 "$srcdir/sddm.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/sddm-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/sddm.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/sddm-longrun/producer-for"
	install -Dm 0644 "$srcdir/sddm.longrun.run" "$pkgdir/etc/s6-serv/available/rc/sddm-longrun/run"
	install -Dm 0644 "$srcdir/sddm.longrun.type" "$pkgdir/etc/s6-serv/available/rc/sddm-longrun/type"
	
	# log
	install -Dm 0644 "$srcdir/sddm.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/sddm-log/consumer-for"
	install -Dm 0644 "$srcdir/sddm.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/sddm-log/dependencies"
	install -Dm 0644 "$srcdir/sddm.log.run" "$pkgdir/etc/s6-serv/available/rc/sddm-log/run"
	install -Dm 0644 "$srcdir/sddm.log.type" "$pkgdir/etc/s6-serv/available/rc/sddm-log/type"
	
	# hook
	install -Dm 0644 "$srcdir/sddm.logd" "$pkgdir/etc/s6-serv/log.d/sddm-rc"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/sddm-s6rcserv/LICENSE"
}
