## Notes

- These files are Bird 1.x compatible:
  - [bird_roa_dn42.conf](bird_roa_dn42.conf)
  - [bird4_roa_dn42.conf](bird4_roa_dn42.conf)
  - [bird6_roa_dn42.conf](bird6_roa_dn42.conf)
- These files are Bird 2.x compatible:
  - [bird_route_dn42.conf](bird_route_dn42.conf)
  - [bird4_route_dn42.conf](bird4_route_dn42.conf)
  - [bird6_route_dn42.conf](bird6_route_dn42.conf)
- These files are [Routinator][2] and [gortr][3] ([src][6]) compatible:
  - [export_rfc8416_dn42.json](export_rfc8416_dn42.json) _(SLURM standard, format specified in [RFC 8416][4])_
- These files are [gortr][3] compatible:
  - [export_dn42.json](export_dn42.json)

Note the gortr source file is DateTime stamped only, it is not signed with any certificaty. So you will need to add
`-verify=false` as a runtime parameter when loading the cache file. Alternatively, use gortr with a slurm file
instead (e.g. ) as a command-line parameter.

## [Last merge commit][0] at [dn42 registry][1]

```
commit e93239341d075ec3f295a38e2b483dc5b2cec9b9
Merge: e668d79b 809f7c00
Author: Simon Marsh <burble@noreply.dn42.us>
Date:   2020-07-15 19:28:35 +0000

    Merge pull request 'Moving to public ASN' (#50) from hertz/registry:hertz-20200715/moving-to-pub-asn into master

    Reviewed-on: https://git.dn42.dev/dn42/registry/pulls/50
```

## crontab

You can setup a [cronjob][5] to check in with updates to the ROA files listed
above on regular intervals.

Currently the ROA files published here is refreshed every 10th hour if
updates has been made to the [DN42 registry][1].

## Misc statistics

- ROAs IPv4:  1262
- ROAs IPv6:  1021
- ROAs total: 2283

[0]: https://git.dn42.us/dn42/registry/commit/e93239341d075ec3f295a38e2b483dc5b2cec9b9
[1]: https://git.dn42.us/dn42/registry
[2]: https://github.com/NLnetLabs/routinator
[3]: https://github.com/cloudflare/gortr
[4]: https://tools.ietf.org/html/rfc8416
[5]: doc/crontab.md
[6]: https://github.com/cloudflare/gortr/#configure-filters-and-overrides-slurm

