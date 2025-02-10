all:
	./tasm6801 -c10 MC10_BASIC_1.ASM
	cp -f MC10_BASIC_1.obj MC10_BASIC_1.ROM
#	cp -f mc10_my.asm mc10_my2.asm
	./f9dasm -6801 MC10_BASIC_1.ROM > MC10_BASIC_1.ASM.TXT
try: all
	/applications/wine6/bin/wine32on64 vmc10.exe
	killall wine64-preloader
	killall wineserver
	ps -A | grep wine

dorgrom:
		./f9dasm -6801 mc10_org.rom > mc10_org.ASM.TXT

