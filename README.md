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

This repository includes indicators for 91 stalkerware applications

* AiSpyer (`aivideoedit.com` `aispyer.com` `www.aispyer.com`)
* AllTracker (`alltracker.org`)
* AndroidLost (`androidlost.com` `www.androidlost.com`)
* AndroidMonitor (`androidmonitor.com` `www.androidmonitor.com`)
* AndroidPolice (`amon.android-monitor.ru` `amon1.android-monitor.ru` `andmon.name` `android-apk.android-monitor.ru` `android-monitor1.android-monitor.ru` `android-police.android-monitor.ru` `android-police.ru` `anmon.android-monitor.ru` `anmon.name` `anmon.ru` `anmon.su` `anmon1.android-monitor.ru` `droimon20.ru` `monitor-android.android-monitor.ru` `prog-money.android-monitor.ru` `prog-money.com` `www.android-monitor.ru`)
* AndroidSpy (`a-spy.com` `www.a-spy.com`)
* AntiFurtoDroid (`antifurtodroid.com`)
* AppMia (`appmia.com` `appmia.com.es` `appmia.it` `appmia.fr` `cp.appmia.com`)
* AppSpy (`app.appspy.net` `app.appspyfree.com` `app.freephonespy.net` `app.freephonespy.net` `app.mobilespyfree.net` `appspy.net` `appspyfree.com` `apptracker.net` `cellphonespyappon.com` `free-spy.com` `free.apptracker.net` `freemobilespy.net` `freephonespy.net` `justseries.net` `mobilespyfree.net` `spyadvice.com` `spyren.com` `trackerfree.net` `www.appspy.net` `www.apptracker.net` `www.cellphonespyappon.com` `www.freemobilespy.net` `www.freephonespy.net` `www.mobilespyfree.net` `www.spyadvice.com` `www.spyren.com` `www.trackerfree.net` `www.xvids.us` `xvids.us`)
* BlurSpy (`www.blurspy.com` `blurspy.com` `xoxospy.com`)
* Bulgok (`c-phone.ru`)
* CallSMSTracker (`callsmstracker.com` `hiddensmstracker.com` `hiddensystemhealth.com` `registrations.smstracker.com` `smstracker.com` `smstrackerweb.com` `www.hiddensmstracker.com` `www.hiddensystemhealth.com` `www.smstrackerweb.com`)
* CatWatchful (`catwatchful.com` `catwatchful.online`)
* Cerberus (`cerberusapp.com` `www.cerberusapp.com`)
* ClevGuard (`clevguard.net`)
* Cocospy (`cocospy.com` `fonemonitor.co` `minspy.com` `neatspy.com` `safespy.com` `spyic.com` `spyine.com` `spyzie.com` `spyzie.io` `spyzie.online` `teensafe.net` `www.fonemonitor.co` `www.minspy.com` `www.spyic.com` `www.spyzie.com` `www.teensafe.net`)
* CouplerTracker (`coupletracker.com`)
* EasyLogger (`logger.mobi` `childsafetytrackerapp.com` `seniorsafetyapp.com` `www.childsafetytrackerapp.com` `www.seniorsafetyapp.com`)
* EasyPhoneTrack (`spappmonitoring.com` `www.spappmonitoring.com` `mobil-kem.com`)
* EspiaoAndroid (`foxspy.com.br`)
* EvaSpy (`evaspy.com` `login.evaspy.com` `spyrix.com` `www.spyrix.com`)
* FamiSafe (`famisafe.wondershare.com` `famisafeapp.wondershare.com` `accounts.wondershare.com`)
* FindMyKids (`findmykids.org` `discount.findmykids.org`)
* FindMyPhone (`find-myphone.com`)
* FlexiSpy (`flexispy.com` `community.flexispy.com` `blog.flexispy.com` `www.flexispy.com`)
* FreeAndroidSpy (`freeandroidspy.com`)
* GPSTrackerLoki (`asgardtech.ru`)
* HelloSpy (`1topspy.com` `hellospy.com` `maxxspy.com` `mobiispy.com` `innovaspy.com`)
* HighsterMobile (`auto-forward.com` `cellphoneservices.info` `ddiutilities.com` `evt17.com` `highstermobile.com` `phonespector.com`)
* Hoverwatch (`br.refog.com` `de.refog.com` `es.refog.com` `fr.refog.com` `hover.watch` `hoverwatch.com` `hu.refog.com` `hws.icu` `it.refog.com` `my.hws.icu` `nl.refog.com` `prospybubble.com` `refog.com` `refog.de` `refog.net` `refog.org` `ro.refog.com` `www.hoverwatch.com`)
* KasperskySafeKids
* KidsControl (`kid-control.com` `kid-control.ru`)
* KidsShield (`backupsoft.eu` `freespyapp.com` `kidsshield.net` `pc.freespyapp.com` `pc.selfspy.com` `selfspy.com` `techinnovative.net` `tifamily.net` `tispy.net` `ua.tispy.net` `www.selfspy.com`)
* LetMeSpy (`letmespy.com` `remotecommands.com` `www.letmespy.com` `www.teleszpieg.pl` `teleszpieg.pl` `bbiindia.com` `www.bbiindia.com`)
* Metasploit (`foreverspy.com`)
* MeuSpy (`servidor.in` `meuspy.com`)
* MobiSpy (`mobispy.net`)
* MobiStealth (`mobistealth.com` `www.mobistealth.com`)
* MobileTool (`mobiletool.ru` `www.mobiletool.ru` `mtoolapp.net` `www.mtoolapp.net` `mtoolapp.biz`)
* MobileTrackerFree (`br.mobile-tracker-free.com` `br.loverman.net` `celltracker.io` `loverman.net` `mobile-tracker-family.com` `mobile-tracker-free.be` `mobile-tracker-free.biz` `mobile-tracker-free.co` `mobile-tracker-free.com` `mobile-tracker-free.de` `mobile-tracker-free.es` `mobile-tracker-free.eu` `mobile-tracker-free.fr` `mobile-tracker-free.info` `mobile-tracker-free.ir` `mobile-tracker-free.it` `mobile-tracker-free.me` `mobile-tracker-free.mobi` `mobile-tracker-free.name` `mobile-tracker-free.net` `mobile-tracker-free.org` `support.mobile-tracker-free.com` `support.loverman.net`)
* NemoSpy (`nemospy.com` `admin.nemospy.com`)
* NeoSpy (`neospy.pro` `neospy.net` `neospy.tech`)
* NetSpy (`www.netspy.net` `netspy.net`)
* OneLocator (`locatorprivacy.com` `onelocator.com`)
* OneMonitar (`onespy.com`)
* OwnSpy (`mobileinnova.net` `ownspy.com` `en.ownspy.com` `webdetetive.com.br` `ownspy.es`)
* PanSpy (`panspy.me` `panspy.com` `surveilstar.com`)
* PhoneSheriff (`www.mobile-spy.com` `www.emobilespy.com` `phonesheriff.com` `www.phonesheriff.com`)
* RealtimeSpy (`www.spytech-web.com` `spytech-web.com` `realtime-spy-mobile.com` `www.realtime-spy-mobile.com`)
* Reptilicus (`reptilicus.net` `thecybernanny.com` `apollospy.com`)
* SecretCamRecorder
* ShadowSpy (`shadow-logs.com` `shadow-spy.com` `www.shadow-logs.com` `www.shadow-spy.com`)
* Snoopza (`snoopza.com` `get.snoopza.com` `snoopza.zendesk.com` `demo.snoopza.com` `newdemo.snoopza.com`)
* Spy24 (`spy24.net`)
* SpyAdvice (`spyadvice.com` `freespyphone.net`)
* SpyApp247
* SpyEra (`spyera.com`)
* SpyHide (`spyhide.com` `www.spyhide.com` `spyhide.ir` `www.spyhide.ir`)
* SpyHuman (`spyhuman.com` `services.spyhuman.com`)
* SpyKontrol (`www.spykontrol.com` `spykontrol.com` `androidapk.biz`)
* SpyLive260 (`spylive360.com` `www.spylive360.com`)
* SpyMasterPro (`spymasterpro.com` `www.spymasterpro.com`)
* SpyMug
* SpyPhoneApp
* SpyToApp (`spytoapp.com`)
* Spyier (`spyier.com`)
* Spymie
* SpyphoneMobileTracker (`phonetracker.com` `www.phonetracker.com` `spyfone.com` `spyphone.com` `www.spyphone.com`)
* TalkLog (`talklog.tools`)
* TheOneSpy (`theonespy.com` `www.theonespy.com`)
* TheTruthSpy (`copy9.com` `exactspy.com` `fonetracker.com` `guestspy.com` `ispyoo.com` `mxspy.com` `phonespying.com` `phonetracking.net` `spyapps.net` `thetruthspy.com` `weysys.com`)
* TrackMyPhones (`trackmyphones.com` `www.trackmyphones.com`)
* TrackView (`chome.zstone.co` `lifecircle.app` `trackview.net` `trackview.recurly.com`)
* TrackingSmartphone (`trackingsmartphone.com` `www.trackingsmartphone.com` `onlinefundb.com`)
* Trackplus (`account.spytomobile.com` `forum.spytomobile.com` `spy2mobile.com` `spytomobile.com` `trackerplus.ru` `www.spy2mobile.com` `www.spytomobile.com`)
* Tracku (`clues4.com` `hike.in` `e-spy.org` `www.e-spy.org`)
* Unisafe (`usafe.ru` `unisafe.su` `unisafe.techmas.ru`)
* VIPTrack (`viptrack.ro`)
* WiseMo (`wisemo.com` `www.wisemo.com`)
* WtSpy (`wtspy.com`)
* XNSpy (`xnspy.com` `cp.xnspy.com`)
* Xnore (`xnore.com`)
* XySpy (`xyspy.com`)
* bark (`bark.us` `www.bark.us`)
* eyeZy (`www.eyezy.com`)
* iKeyMonitor (`easemon.com`)
* iMonitorSpy (`www.imonitorsoft.cn` `www.imonitorsoft.com` `imonitorsoft.cn`)
* jjspy (`www.jjspy.com` `www.ttspy.com`)
* mSpy (`www.mspyonline.com` `mspyonline.com` `mspylite.com` `mspy.nl` `mspy.co.uk` `mspy.net` `mspy.in` `mspy.it` `mspy.jp` `mspy.com.br` `mliteapp.com`)
* pcTattletale (`www.pctattletale.com`)
* uMobix (`umobix.com`)

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



