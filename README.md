# Awesome Password Cracking	 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of awesome tools, research, papers and other projects related to password cracking and password security.



Read [CONTRIBUTING.md](https://github.com/narkopolo/awesome-password-cracking/blob/main/CONTRIBUTING.md) before contributing! In short:

- List is alphabetically sorted
- If in doubt, use [awesome-lint](https://github.com/sindresorhus/awesome-lint)
- If you think an item shouldn't be here [open an issue](https://github.com/narkopolo/awesome-password-cracking/issues/new)



## Contents

- [Books](#books)
- [Cloud](#cloud)
- [Conversion](#conversion)
- [Hashcat](#hashcat)
  - [Automation](#automation)
  - [Distributed cracking](#distributed-cracking)
  - [Rules](#rules)
  - [Rule tools](#rule-tools)
  - [Web interfaces](#web-interfaces)
- [John the Ripper](#john-the-ripper)
- [Misc](#misc)
- [Websites](#websites)
  - [Communities](#communities)
  - [Lookup services](#lookup-services)
- [Wordlist tools](#wordlist-tools)
  - [Analysis](#analysis)
  - [Generation/Manipulation](#generationmanipulation)
- [Wordlists](#wordlists)
  - [Laguage specific](#laguage-specific)
  - [Other](#other)
- [Specific file formats](#specific-file-formats)
  - [PDF](#pdf)
  - [PEM](#pem)
  - [JKS](#jks)
  - [ZIP](#zip)
- [Artificial Intelligence](#artificial-intelligence)
- [Research](#research)
  - [Papers](#papers)
  - [Talks](#talks)



## Books
- [Hash Crack: Password Cracking Manual (v3)](https://www.amazon.com/-/en/Joshua-Picolet/dp/1793458618) - Password Cracking Manual v3 is an expanded reference guide for password recovery (cracking) methods, tools, and analysis techniques.



## Cloud
- [Cloud_crack](https://github.com/lordsaibat/Cloud_crack) - Crack passwords using Terraform and AWS.
- [Cloudcat](https://github.com/stormfleet/cloudcat) - A script to automate the creation of cloud infrastructure for hash cracking.
- [Cloudstomp](https://github.com/Fmstrat/cloudstomp) - Automated deployment of instances on EC2 via plugin for high CPU/GPU applications at the lowest price.
- [Cloudtopolis](https://github.com/JoelGMSec/Cloudtopolis) - A tool that facilitates the installation and provisioning of Hashtopolis on the Google Cloud Shell platform, quickly and completely unattended (and also, free!).
- [NPK](https://github.com/c6fc/npk) - NPK is a distributed hash-cracking platform built entirely of serverless components in AWS including Cognito, DynamoDB, and S3.
- [Penglab](https://github.com/mxrch/penglab) - Abuse of Google Colab for cracking hashes.
- [Rook](https://github.com/JumpsecLabs/Rook) - Automates the creation of AWS p3 instances for use in GPU-based password cracking.


## Conversion
- [7z2hashcat](https://github.com/philsmd/7z2hashcat) - Extract information from password-protected .7z archives (and .sfx files) such that you can crack these "hashes" with hashcat.
- [MacinHash](https://github.com/jmagers/MacinHash) - Convert macOS plist password file to hash file for password crackers.
- [NetNTLM-Hashcat](https://github.com/ins1gn1a/NetNTLM-Hashcat) - Converts John The Ripper/Cain format hashes (singular, or in bulk) to HashCat compatible hash format.
- [Rubeus-to-Hashcat](https://github.com/PwnDexter/Rubeus-to-Hashcat) - Converts / formats Rubeus kerberoasting output into hashcat readable format.
- [WINHELLO2hashcat](https://github.com/Banaanhangwagen/WINHELLO2hashcat) - With this tool one can extract the "hash" from a WINDOWS HELLO PIN. This hash can be cracked with Hashcat.
- [bitwarden2hashcat](https://github.com/0x6470/bitwarden2hashcat) - A tool that converts Bitwarden's data into a hashcat-suitable hash.
- [hc\_to\_7z](https://github.com/philsmd/hc_to_7z) - Convert 7-Zip hashcat hashes back to 7z archives.
- [hcxtools](https://github.com/ZerBea/hcxtools) - Portable solution for conversion of cap/pcap/pcapng (gz compressed) WiFi dump files to hashcat formats.
- [itunes_backup2hashcat](https://github.com/philsmd/itunes_backup2hashcat) - Extract the information needed from the Manifest.plist files to convert it to hashes compatible with hashcat.	
- [mongodb2hashcat](https://github.com/philsmd/mongodb2hashcat) - Extract hashes from the MongoDB database server to a hash format that hashcat accepts: -m 24100 (SCRAM-SHA-1) or -m 24200 (SCRAM-SHA-256).



## Hashcat
*[Hashcat](https://github.com/hashcat/hashcat) is the "World's fastest and most advanced password recovery utility." The following are projects directly related to Hashcat in one way or another.*

- [Autocrack](https://github.com/pry0cc/autocrack) - A set of client and server tools for automatically, and lightly automatically cracking hashes.
- [docker-hashcat](https://github.com/dizcza/docker-hashcat) - Latest hashcat docker for Ubuntu 18.04 CUDA, OpenCL, and POCL.
- [Hashcat-Stuffs](https://github.com/xfox64x/Hashcat-Stuffs) - Collection of hashcat lists and things.
- [hashcat-utils](https://github.com/hashcat/hashcat-utils/) - Small utilities that are useful in advanced password cracking.
- [Hashfilter](https://github.com/bharshbarger/Hashfilter) - Read a hashcat potfile and parse different types into a sqlite database.
- [known_hosts-hashcat](https://github.com/chris408/known_hosts-hashcat) - A guide and tool for cracking ssh known_hosts files with hashcat.
- [pyhashcat](https://github.com/f0cker/pyhashcat) - Python C API binding to libhashcat.


### Automation
- [autocrack](https://github.com/timbo05sec/autocrack) - Hashcat wrapper to help automate the cracking process.
- [hashcat.launcher](https://github.com/s77rt/hashcat.launcher) - A cross-platform app that run and control hashcat.
- [hat](https://github.com/sp00ks-git/hat) - An Automated Hashcat Tool for common wordlists and rules to speed up the process of cracking hashes during engagements.
- [hate_crack](https://github.com/trustedsec/hate_crack) - A tool for automating cracking methodologies through Hashcat from the TrustedSec team.
- [Naive hashcat](https://github.com/brannondorsey/naive-hashcat) - Naive hashcat is a plug-and-play script that is pre-configured with naive, emperically-tested, "good enough" parameters/attack types.

### Distributed cracking
- [CrackLord](https://github.com/jmmcatee/cracklord) - Queue and resource system for cracking passwords.
- [fitcrack](https://github.com/nesfit/fitcrack) - A hashcat-based distributed password cracking system.
- [Hashtopolis](https://github.com/hashtopolis/server) - A multi-platform client-server tool for distributing hashcat tasks to multiple computers.
- [HashtopoloCLI](https://github.com/jakewnuk/HashtopoCLI) - CLI tool for Hashtopolis API incorporating some of the API functionality into a dynamic Python wrapper.
- [Kraken](https://github.com/arcaneiceman/kraken) - A multi-platform distributed brute-force password cracking system.

### Rules
- [clem9669 rules](https://github.com/clem9669/hashcat-rule) - Rule for hashcat or john.
- [hashcat rules collection](https://github.com/narkopolo/hashcat-rules-collection) - Probably the largest collection of hashcat rules out there.
- [Hob0Rules](https://github.com/praetorian-inc/Hob0Rules) - Password cracking rules for Hashcat based on statistics and industry patterns.
- [Kaonashi](https://github.com/kaonashi-passwords/Kaonashi) - Wordlist, rules and masks from Kaonashi project (RootedCON 2019).
- [nsa-rules](https://github.com/NSAKEY/nsa-rules) - Password cracking rules and masks for hashcat generated from cracked passwords.
- [nyxgeek-rules](https://github.com/nyxgeek/nyxgeek-rules) - Custom password cracking rules for Hashcat and John the Ripper.
- [OneRuleToRuleThemAll](https://github.com/NotSoSecure/password_cracking_rules) - "One rule to crack all passwords. or atleast we hope so."
- [pantagrule](https://github.com/rarecoil/pantagrule) - Large hashcat rulesets generated from real-world compromised passwords.
- [squid rules](https://github.com/jakewnuk/HIBP-578M) - Hashcat rules ordered by effectiveness from testing HIBPv7.

### Rule tools
- [duprule](https://github.com/mhasbini/duprule) - Detect & filter duplicate hashcat rules.


### Web interfaces
- [crackerjack](https://github.com/ctxis/crackerjack) - CrackerJack is a Web GUI for Hashcat developed in Python.
- [CrackQ](https://github.com/f0cker/crackq) - A Python Hashcat cracking queue system.
- [hashpass](https://github.com/dj-zombie/hashpass) - Hash cracking WebApp & Server for hashcat.
- [Hashview](https://github.com/hashview/hashview) - A web front-end for password cracking and analytics.
- [Wavecrack](https://github.com/wavestone-cdt/wavecrack) - Wavestone's web interface for password cracking with hashcat.
- [WebHashCat](https://github.com/hegusung/WebHashcat) - WebHashcat is a very simple but efficient web interface for hashcat password cracking tool.



## John the Ripper
*[John the Ripper](https://github.com/openwall/john) is "an Open Source password security auditing and password recovery tool available for many operating systems." The following are projects directly related to John the Ripper in one way or another.*

- [BitCracker](https://github.com/e-ago/bitcracker) - BitCracker is the first open source password cracking tool for memory units encrypted with BitLocker.
- [johnny](https://github.com/openwall/johnny) - GUI frontend to John the Ripper.



## Misc
- [920mPasswordMasks](https://github.com/jakewnuk/920mPasswordMasks) - Hashcat password masks from 920 million breach passwords filtered into groups.
- [hashID](https://github.com/psypanda/hashID) - Software to identify the different types of hashes.
- [Name That Hash](https://github.com/HashPals/Name-That-Hash) - Don't know what type of hash it is? Name That Hash will name that hash type! Identify MD5, SHA256 and 300+ other hashes. Comes with a neat web app.


## Websites

### Communities
- [hashcat Forum](https://hashcat.net/forum/) - Forum by the developers of hashcat.
- [Hashmob](https://hashmob.net/) - A growing password recovery community aimed towards being a center point of collaboration for cryptography enthusiasts.
- [Hashkiller Forum](https://forum.hashkiller.io/) - A password cracking forum with over 20,000 registered users.

### Lookup services
- [CMD5](https://www.cmd5.org/) - Provides online MD5 / sha1/ mysql / sha256 encryption and decryption services.
- [CrackStation](https://crackstation.net/) - Free hash lookup service supplying wordlists as well.
- [Hashes.com](https://hashes.com/) - A hash lookup service with paid features.
- [Hashkiller](https://hashkiller.io/) - A hash lookup service with a forum.
- [Online Hash Crack](https://www.onlinehashcrack.com/) - Cloud password recovery service.



## Wordlist tools
*Tools for analyzing, generating and manipulating wordlists.*

### Analysis
- [PACK](https://github.com/iphelix/pack) - A collection of utilities developed to aid in analysis of password lists in order to enhance password cracking through pattern detection of masks, rules, character-sets and other password characteristics.
- [pcfg_cracker](https://github.com/lakiw/pcfg_cracker) - This project uses machine learning to identify password creation habits of users.
- [Pipal](https://github.com/digininja/pipal) - THE password analyser.
- [PwdStat](https://github.com/jakewnuk/pwdstat) - Tool for identifying systemic password usage, creating password masks, and analyzing cracked password samples with human readable statistics to help defenders.


### Generation/Manipulation

- [common-substr](https://github.com/sensepost/common-substr) - Simple tool to extract the most common substrings from an input text. Built for password cracking.
- [Crunch](https://sourceforge.net/projects/crunch-wordlist/) - Crunch is a wordlist generator where you can specify a standard character set or a character set you specify. Crunch can generate all possible combinations and permutations.
- [CUPP](https://github.com/Mebus/cupp) - A tool that lets you generate wordlists by user profiling data such as birthday, nickname, address, name of a pet or relative etc.
- [duplicut](https://github.com/nil0x42/duplicut) - Remove duplicates from MASSIVE wordlist, without sorting it (for dictionary-based password cracking).
- [Gorilla](https://github.com/d4rckh/gorilla) - Tool for generating wordlists or extending an existing one using mutations.
- [Keyboard-Walk-Generators](https://github.com/Rich5/Keyboard-Walk-Generators) - Generate Keyboard Walk Dictionaries for cracking.
- [kwprocessor](https://github.com/hashcat/kwprocessor) - Advanced keyboard-walk generator with configureable basechars, keymap and routes.
- [maskcat](https://github.com/jakewnuk/maskcat) - Utility tool for Hashcat Masks and Password Cracking
- [maskprocessor](https://github.com/hashcat/maskprocessor/) - High-performance word generator with a per-position configureable charset.
- [maskuni](https://github.com/flbdx/maskuni) - A standalone fast word generator in the spirit of hashcat's mask generator with unicode support.
- [Mentalist](https://github.com/sc0tfree/mentalist) - Mentalist is a graphical tool for custom wordlist generation. It utilizes common human paradigms for constructing passwords and can output the full wordlist as well as rules compatible with Hashcat and John the Ripper.
- [Phraser](https://github.com/Sparell/Phraser) - Phraser is a phrase generator using n-grams and Markov chains to generate phrases for passphrase cracking.
- [princeprocessor](https://github.com/hashcat/princeprocessor) - Standalone password candidate generator using the PRINCE algorithm.
- [Rephraser](https://github.com/travco/rephraser) - A Python-based reimagining of Phraser using Markov-chains for linguistically-correct password cracking.
- [Rling](https://github.com/Cynosureprime/rling) - RLI Next Gen (Rling), a faster multi-threaded, feature rich alternative to rli found in hashcat utilities.
- [statsprocessor](https://github.com/hashcat/statsprocessor/) - Word generator based on per-position markov-chains.
- [TTPassGen](https://github.com/tp7309/TTPassGen) - Flexible and scriptable password dictionary generator which supportss brute-force, combination, complex rule modes etc.
- [token-reverser](https://github.com/dariusztytko/token-reverser) - Words list generator to crack security tokens.
- [WikiRaider](https://github.com/NorthwaveSecurity/wikiraider) - WikiRaider enables you to generate wordlists based on country specific databases of Wikipedia.




## Wordlists
### Laguage specific
- [Albanian wordlist](https://github.com/its0x08/albanian-wordlist) - A mix of names, last names and some albanian literature.
- [Danish Phone Wordlist Generator](https://github.com/narkopolo/danish_phone_wordlist_generator) - This tool can generate wordlists of Danish phone numbers by area and/or usage (Mobile, landline etc.) Useful for password cracking or fuzzing Danish targets.
- [Danish Wordlists](https://github.com/narkopolo/danish-wordlists) - Collection of danish wordlists for cracking danish passwords.
- [French Wordlists](https://github.com/clem9669/wordlists) - This project aim to provide french word list about everything a person could use as a base password.

### Other
- [Packet Storm Wordlists](https://packetstormsecurity.com/Crackers/wordlists/page1/) - A substantial collection of different wordlists in multiple languages.
- [Rocktastic](https://labs.nettitude.com/tools/rocktastic/) - Includes many permutations of passwords and patterns that have been observed in the wild.
- [RockYou2021](https://github.com/ohmybahgosh/RockYou2021.txt) - 	RockYou2021.txt is a MASSIVE WORDLIST compiled of various other wordlists.
- [WeakPass](https://weakpass.com/) - Collection of large wordlists.



## Specific file formats
### PDF
- [pdfrip](https://github.com/mufeedvh/pdfrip) - A multi-threaded PDF password cracking utility equipped with commonly encountered password format builders and dictionary attacks.

### PEM
- [pemcracker](https://github.com/bwall/pemcracker) - Tool to crack encrypted PEM files.

### JKS
- [JKS private key cracker](https://github.com/floyd-fuh/JKS-private-key-cracker-hashcat) - Cracking passwords of private key entries in a JKS fileCracking passwords of private key entries in a JKS file.

### ZIP
- [bkcrack](https://github.com/kimci86/bkcrack) - Crack legacy zip encryption with Biham and Kocher's known plaintext attack.
- [frackzip](https://github.com/hyc/fcrackzip) - Small tool for cracking encrypted ZIP archives.



## Artificial Intelligence
- [adams](https://github.com/TheAdamProject/adams) - Reducing Bias in Modeling Real-world Password Strength via Deep Learning and Dynamic Dictionaries.
[](https://github.com/cupslab/neural_network_cracking) - Code for cracking passwords with neural networks.
- [RNN-Passwords](https://github.com/gehaxelt/RNN-Passwords) - Using the char-rnn to learn and guess passwords.
- [rulesfinder](https://github.com/synacktiv/rulesfinder) - This tool finds efficient password mangling rules (for John the Ripper or Hashcat) for a given dictionary and a list of passwords.



## Research

### Papers
- [Generating Optimized Guessing Candidates toward Better Password Cracking from Multi-Dictionaries Using Relativistic GAN (2020)](https://www.mdpi.com/2076-3417/10/20/7306/htm)
- [GENPass: A General Deep Learning Model for Password Guessing with PCFG Rules and Adversarial Generation (2018)](https://ieeexplore.ieee.org/document/8422243)
- [Password Cracking Using Probabilistic Context-Free Grammars (2009)](https://www.researchgate.net/publication/220713709_Password_Cracking_Using_Probabilistic_Context-Free_Grammars)
- [Reducing Bias in Modeling Real-world Password Strength via Deep Learning and Dynamic Dictionaries (2020)](https://arxiv.org/abs/2010.12269)
- [Fast, Lean, and Accurate: Modeling Password Guessability Using Neural Networks (2016)](https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/melicher)
- [PassGAN: A Deep Learning Approach for Password Guessing (2017)](https://arxiv.org/pdf/1709.00440)

### Talks
- [DEF CON Safe Mode Password Village - Getting Started with Hashcat](https://www.youtube.com/watch?v=MBTJ8f6Fsmg)
- [DEF CON Safe Mode Password Village - Jeremi Gosney - Cracking at Extreme Scale](https://www.youtube.com/watch?v=4Ell1Tt23NI)
- [Tailored, Machine Learning-driven Password Guessing Attacks and Mitigation at DefCamp](https://www.youtube.com/watch?v=iK6ZbD6v9Gg)
- [UNHash - Methods for better password cracking](https://media.ccc.de/v/31c3_-_5966_-_en_-_saal_1_-_201412292245_-_unhash_-_methods_for_better_password_cracking_-_tonimir_kisasondi)
- [USENIX Security '21 - Reducing Bias in Modeling Real-world Password Strength via Deep Learning and Dynamic Dictionaries](https://www.youtube.com/watch?v=Jvp3UTdCeag)
- [USENIX Security '16 - Fast, Lean, and Accurate: Modeling Password Guessability Using Neural Networks
](https://www.youtube.com/watch?v=GgaZ_LxsL_8)
