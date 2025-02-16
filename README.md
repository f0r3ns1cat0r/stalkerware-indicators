# Stalkerware Indicators of Compromise

Indicators of compromise (IOC) on Stalkerware applications for Android and iOS

_Warning: these indicators are not providing a complete detection of
stalkerware applications. They are based on research from a few people on their
free time and many apps are likely missing. Use it carefully. No detection
based on these indicators should not be understood as having no stalkerware
installed._

## What's a stalkerware?

We're using the definition of the [Coalition Against Stalkerware](https://stopstalkerware.org/):

> Stalkerware refers to tools – software programs, apps and devices – that
enable someone to secretly spy on another person’s private life via their
mobile device. The abuser can remotely monitor the whole device including web
searches, geolocation, text messages, photos, voice calls and much more. Such
programs are easy to buy and install. They run hidden in the background,
without the affected person knowing or giving their consent. Regardless of
stalkerware’s availability, the abuser is accountable for using it as a tool
and hence for committing this crime.

## IOC

Main files:

* `ioc.yaml` : Indicators of compromise of many Stalkerware apps. Includes
    * [Applications Package names](https://support.google.com/admob/answer/9972781)
    * [Android Application Certificates](https://support.google.com/googleplay/android-developer/answer/9842756?hl=en)
    * List of websites
    * List of domains and IPs of [C2](https://en.wikipedia.org/wiki/Botnet#Command_and_control)
* `quad9_blocklist.txt`: blocklist for [Quad9 DNS resolver](https://www.quad9.net/) (include a more limited set of domains for apps clearly for stalking and only C2 domains, not app websites)
* `samples.csv`: List of samples with hashes, package name, certificate and version.

Files generated automatically from previous IOC files:

* `generated/hosts`: network indicators (C2 domains only) in hosts format
* `generated/indicators-for-tinycheck.json`: indicators in [TinyCheck](https://github.com/KasperskyLab/TinyCheck) compatible format
* `generated/misp_event.json`: indicators in [MISP](https://www.misp-project.org/) compatible format
* `generated/network.csv`: network indicators in a more grepable CSV format
* `generated/stalkerware.stix2`: indicators in [STIX2](https://oasis-open.github.io/cti-documentation/stix/intro) format
* `generated/suricata.rules`: [Suricata](https://suricata.io/) rules for network indicators (C2 only)

Scripts:
* `scripts/check_apk.py`: check an APK file or APKs in a folder with the indicators from this repository
* `scripts/generate.py`: creates all the files in the `generated` folder (automatically done through github actions)
* `scripts/linter.py`: linter to check the format of the different indicator files (automtaically done through github actions)

## Stalkerware

This repository includes indicators for the following stalkerware :

* 1TopSpy : `www.1topspy.com`
* AirSpyer
* AllTracker : `alltracker.org` (also called [Russ City](https://www.zscaler.com/blogs/security-research/new-wave-stalkerware-apps))
* AndroidLost : `androidlost.com`
* AntiFurto Droid : `antifurtodroid.com`
* AppMia
* AppSpy : `www.appspy.com`
* Android Monitor : `www.androidmonitor.com`
* Bark : `www.bark.us`
* BlurSpy : `www.blurspy.com`
* CallSMSTracker : `callsmstracker.com`
* Catwatchful : `catwatchful.com`
* Cerberus : `www.cerberusapp.com`
* ClevGuard : `www.clevguard.com`
* Cocospy : `www.cocospy.com`
* Copy9 : `copy9.com`
* DDI Utilities : `ddiutilities.com`
* EasyLogger : `logger.mobi`
* EasyPhoneTrack : `easyphonetrack.com` (also `spappmonitoring.com`)
* Espiao Android: `espiaoandroid.com.br`
* EyeZy : `www.eyezy.com`
* FlexiSpy : `www.flexispy.com`
* Free Android Spy : `www.freeandroidspy.com`
* FoneTracker : `fonetracker.com`
* FoneMonitor : `fonemonitor.co`
* ForeverSpy : `foreverspy.com`
* GPSTrackerLoki : `asgardtech.ru`
* GuestSpy : `guestspy.com` (now replaced by TheTruthSpy)
* HelloSpy : `hellospy.com`
* Highster Mobile : `highstermobile.com`
* Hoverwatch : `www.hoverwatch.com`
* iKeyMonitor : `ikeymonitor.com`
* iMonitorSpy : `www.imonitorsoft.com`
* iSpyoo : `ispyoo.com`
* LetMeSpy : `www.letmespy.com`
* Maxxspy: `maxxSpy.com`
* Meuspy: `meuspy.com`
* MinSpy : `minspy.com` (also called kuuvv, cocospy, spyier, …)
* Mobispy : `www.mobispy.net`
* Mobiispy : `mobiispy.com`
* MobileTrackerFree : `mobile-tracker-free.com`
* MobileTool : `mtoolapp.net`, `mobiletool.ru` and `mtoolapp.biz`
* Mobistealth : `www.mobistealth.com`
* mSpy : `www.mspy.com` (also called SpyBubble)
* MxSpy : `mxspy.com`
* NeatSpy : `neatspy.com`
* NetSpy : `www.netspy.net`
* NeoSpy : `neospy.net` (an analysis [here](https://www.zscaler.com/blogs/security-research/spyware-presence-enterprise-networks))
* OneMonitar : `onemonitar.com` (also known as OneSpy)
* OwnSpy : `en.ownspy.com`
* pcTattletale : `www.pctattletale.com`
* PhoneSpying : `www.phonespying.com`
* PhoneSherif : `phonesheriff.com`
* PanSpy : `panspy.com`
* Repticulus : `reptilicus.net`
* SafeSpy : `safespy.com`
* SAP4Mobile : `sap4mobile.com`
* ShadowSpy : `www.shadow-spy.com`
* Snoopza : `snoopza.com`
* Spy24 : `spy24.app`
* SpyApp247 : `www.spyapp247.com`
* SpyEra : `spyera.com`
* SpyHide : `spyhide.com`
* SpyHuman : `spyhuman.com`
* Spyic : `spyic.com`
* Spyier : `spyier.com`
* Spyine : `spyine.com`
* Spylive360 : `spylive360.com`
* SpyMasterPro : `spymasterpro.com`
* Spymie : `www.spymie.com` (analyzed by [ZScaler here](https://www.zscaler.com/blogs/research/why-you-shouldnt-trust-safe-spying-apps))
* SpyPhoneApp : `spyphoneapp.org`
* Spytoapp : `spytoapp.com`
* Spyzie : `www.spyzie.com` `spyzie.io`
* spy2mobile : `spytomobile.com`
* TalkLog : `talklog.tools`
* The One Spy : `theonespy.com`
* TheTruthSpy : `thetruthspy.com`
* TrackMyFone : `trackmyfone.com`
* Track My Phones : `trackmyphones.com`
* uMobix : `umobix.com`
* WiseMo : `www.wisemo.com`
* WtSpy : `wt-spy.com`
* Xnore : `xnore.com`
* XNSpy : `xnspy.com`

## Contributions

This repository is maintained by the [Echap](https://echap.eu.org/) non-profit organisation.

Contributors include:

- [Abir Ghattas](https://twitter.com/AbirGhattas)
- [Anne Roth](https://twitter.com/annalist)
- [Jo Coscia](https://github.com/jcoscia)
- [Julien Voisin](https://dustri.org/)
- [Esther](https://twitter.com/U039b)
- [Jurre van Bergen](https://twitter.com/DrWhax)
- [@nscrutables](https://twitter.com/nscrutables)

These indicators were largely based on research and analysis using [APKlab](https://www.apklab.io/), [Koodous](https://koodous.com/) and [VirusTotal](https://www.virustotal.com/).

## Please Contribute

This repository is not complete, new stalkerware apps appear and disappear all the time. Feel free to contribute to this database by opening an issue or submitting a Pull Request.

If you want to do further research on some apps and need access to the samples, feel free to [send me an email](https://www.randhome.io/contact/).

## Other stalkerware repositories

There are other repositories gathering stalkerware indicators:
* [ch33r10 stalkerware list](https://github.com/ch33r10/Stalkerware/tree/master/IOCs)
* [astryzia](https://github.com/astryzia/stalkerware-urls)
* [diskurse android stalkerware](https://github.com/diskurse/android-stalkerware)
* [TinyCheck IOCs](https://github.com/KasperskyLab/TinyCheck/blob/main/assets/iocs.json)

## References

* [Coalition against stalkerware](https://stopstalkerware.org/)
* [Resources from the Clinic to End Tech Abuse](https://www.ceta.tech.cornell.edu/resources)
* [The Predator in Your Pocket - A Multidisciplinary Assessment of the Stalkerware Application Industry](https://citizenlab.ca/2019/06/the-predator-in-your-pocket-a-multidisciplinary-assessment-of-the-stalkerware-application-industry/) by the Citizen Lab
* [What you need to know about stalkerware](https://www.ted.com/talks/eva_galperin_what_you_need_to_know_about_stalkerware/transcript?language=en) - TED Talk by Eva Galperin

## License

The content of this repository is licensed under [CC0](https://creativecommons.org/share-your-work/public-domain/cc0/),
you're free to do whatever you want with it.

Please note that while we're doing our very best, there is no guarantee that it is accurate.
If it is useful to you, consider giving money to an organisation supporting violence against women in your country.
