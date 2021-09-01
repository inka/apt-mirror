# apt-mirror

steamboatid's fork of apt-mirror

For official source, see: http://apt-mirror.github.com

## Usage

Basic execution:

```
# To run with default paths and values (e.g /etc/apt/mirror.list)
./apt-mirror
# To run using ./mirror.list
./apt-mirror mirror.list
# Or:
perl ./apt-mirror mirror.list
```

apt-mirror can also be installed with

`make install`

See also:

`perldoc ./apt-mirror`

## Changes from apt-mirror/apt-mirror

- Coded at debian buster 10.10
- Some new features added :
	- new config option "use_proxy"  (PR #48)
	- new config option "http_proxy"  (PR #48)
	- new config option "proxy_user"  (PR #48)
	- new config option "proxy_password"  (PR #48)
	- new config option "user_agent"  (fixes #146)
	- new config option "timeout"
		previously hard-coded, now the setup will affect on read, dns and connect timeout
	- new config option "tries"
		previously hard-coded
	- new config option "cookies_file"
		some server provide cookies, so we should provide cookies to legitimate cookie-full servers
	- new config option "dry_run" (PR #86)
	- new config option "max_redirect"
		reducing redirect attempt, to fasten Wget
	- new config option "ip_v6"
		some network problematic with ipv6
	- merge pull request (PR) #36, #40, #48, #77, #86, #95, #96, #100, #103, #105, #111,
		#112, #115, #116, #120, #127, #131, #136, #143
	- bz2 or xz or gz (buster-backports i18n xz) (fixes #130)
	- port number (fixes #19)
