export CC=gcc
export RM=rm -f
export AR=ar cr
export MV=mv
export RANLIB=ranlib
export SED=sed


export SHELL=/bin/sh

INCFLAGS=-I. -I.. -I../include

CFLAGS=-O3 -w $(INCFLAGS) 
#Pentium 4 (Intel)
#CFLAGS=-march=pentium4 -O3 -pipe -fomit-frame-pointer $(INCFLAGS)
#Athlon XP (AMD)
#CFLAGS="-march=athlon-xp -O3 -pipe -fomit-frame-pointer" $(INCFLAGS)
#Athlon64��
#CFLAGS="-O2 -march=athlon64 -ftracer -fprefetch-loop-arrays -pipe" $(INCFLAGS)

PROG=libchar.a

SRC=char_base.c char.c char_event.c char_data.c skill.c title.c\
addressbook.c chatmagic.c event.c char_walk.c encount.c pet.c \
enemy.c pet_event.c char_talk.c char_party.c char_item.c \
petmail.c trade.c family.c

OBJ=$(SRC:.c=.o)

ifeq (0,$(MAKELEVEL))
CC=gcc
RM=rm -f
AR=ar cr
MV=mv
RANLIB=ranlib
SED=sed
SHELL=/bin/sh
endif

all: $(PROG)

$(PROG): $(OBJ)
	$(RM) $(PROG)
	$(AR) $(PROG) $(OBJ)
	$(RANLIB) $(PROG)

dos2unix:
	dos2unix $(SRC) makefile

chmod:
	chmod 777 $(SRC) makefile
	
depend:
	$(MV) makefile makefile.bak
	$(SED) -ne '1,/^# DO NOT DELETE THIS LINE/p' makefile.bak>makefile
	$(CC) $(INCFLAGS) -M $(SRC) >> makefile 

clean:
	$(RM) $(PROG)
	$(RM) $(OBJ)
	$(RM) *~

distclean:
	$(RM) $(PROG)
	$(RM) $(OBJ)
	$(RM) *~
	$(MV) makefile makefile.bak
	$(SED) -ne '1,/^# DO NOT DELETE THIS LINE/p' makefile.bak>makefile
	$(RM) makefile.bak

# DO NOT DELETE THIS LINE
char_base.o: char_base.c ../include/version.h ../include/correct_bug.h \
  ../include/char_base.h \
  ../include/version.h ../include/skill.h ../include/common.h \
  ../include/util.h \
  ../include/title.h \
  ../include/addressbook.h ../include/net.h \
  ../include/char_data.h \
  ../include/item.h ../include/char.h ../include/char_base.h \
  ../include/char_data.h ../include/item.h ../include/buf.h \
  ../include/magic.h ../include/function.h ../include/npccreate.h \
  ../include/configfile.h ../include/title.h ../include/pet.h \
  ../include/pet_skill.h ../include/anim_tbl.h ../include/enemy.h \
  ../include/saacproto_cli.h ../include/saacproto_util.h \
  ../include/log.h
char.o: char.c ../include/version.h ../include/correct_bug.h \
  ../include/net.h ../include/common.h \
  ../include/common.h ../include/char_base.h \
  ../include/version.h ../include/skill.h ../include/util.h \
  ../include/title.h ../include/addressbook.h ../include/net.h \
  ../include/char_data.h ../include/item.h ../include/char.h \
  ../include/char_base.h ../include/char_data.h ../include/char.h \
  ../include/lssproto_serv.h ../include/lssproto_util.h \
  ../include/item.h ../include/item_event.h \
  ../include/buf.h ../include/object.h ../include/map_deal.h \
  ../include/saacproto_cli.h ../include/saacproto_util.h \
  ../include/readmap.h ../include/handletime.h ../include/char_event.h \
  ../include/npccreate.h ../include/addressbook.h ../include/magic_base.h \
  ../include/magic.h ../include/chatmagic.h ../include/configfile.h \
  ../include/log.h ../include/anim_tbl.h ../include/encount.h \
  ../include/battle.h ../include/pet_skill.h ../include/util.h \
  ../include/enemy.h ../include/npcutil.h ../include/pet.h \
  ../include/family.h ../include/correct_bug.h
char_event.o: char_event.c ../include/version.h ../include/correct_bug.h \
  ../include/common.h \
  ../include/char.h ../include/common.h ../include/char_base.h \
  ../include/version.h ../include/skill.h ../include/util.h \
  ../include/title.h ../include/addressbook.h \
  ../include/net.h \
  ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/item_event.h ../include/net.h \
  ../include/item.h ../include/object.h ../include/lssproto_serv.h \
  ../include/lssproto_util.h \
  ../include/util.h \
  ../include/char_data.h ../include/readmap.h ../include/map_deal.h \
  ../include/saacproto_cli.h ../include/saacproto_util.h \
  ../include/npccreate.h ../include/handletime.h ../include/anim_tbl.h \
  ../include/family.h
char_data.o: char_data.c ../include/version.h ../include/correct_bug.h \
  ../include/readmap.h \
  ../include/common.h \
  ../include/util.h \
  ../include/common.h ../include/util.h \
  ../include/anim_tbl.h ../include/battle.h ../include/net.h \
  ../include/char.h ../include/char_base.h \
  ../include/version.h ../include/skill.h ../include/title.h \
  ../include/addressbook.h ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/char_data.h ../include/buf.h \
  ../include/item.h ../include/log.h ../include/pet.h ../include/enemy.h \
  ../include/char_base.h ../include/configfile.h \
  ../include/defaultPlayer.h ../include/family.h \
  ../include/saacproto_cli.h ../include/saacproto_util.h \
  /usr/include/getopt.h
skill.o: skill.c ../include/version.h ../include/correct_bug.h \
  ../include/skill.h \
  ../include/common.h \
  ../include/util.h \
  ../include/util.h ../include/char.h ../include/char_base.h \
  ../include/version.h ../include/skill.h ../include/title.h \
  ../include/addressbook.h ../include/net.h \
  ../include/char_data.h \
  ../include/item.h ../include/char.h
title.o: title.c ../include/version.h ../include/correct_bug.h \
  ../include/title.h ../include/common.h \
  ../include/util.h \
  ../include/char.h ../include/char_base.h ../include/version.h \
  ../include/skill.h ../include/title.h ../include/addressbook.h \
  ../include/net.h \
  ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/char_base.h ../include/item.h \
  ../include/skill.h ../include/buf.h ../include/util.h \
  ../include/configfile.h
addressbook.o: addressbook.c ../include/version.h \
  ../include/correct_bug.h \
  ../include/addressbook.h ../include/common.h \
  ../include/util.h \
  ../include/net.h \
  ../include/char.h ../include/char_base.h \
  ../include/version.h ../include/skill.h ../include/title.h \
  ../include/addressbook.h ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/handletime.h ../include/buf.h \
  ../include/net.h ../include/lssproto_serv.h ../include/lssproto_util.h \
  ../include/saacproto_cli.h ../include/saacproto_util.h \
  ../include/object.h ../include/battle.h ../include/configfile.h \
  ../include/npcutil.h ../include/pet.h ../include/petmail.h \
  ../include/log.h
chatmagic.o: chatmagic.c ../include/version.h ../include/correct_bug.h \
  ../include/common.h \
  ../include/char.h ../include/common.h \
  ../include/char_base.h ../include/version.h ../include/skill.h \
  ../include/util.h \
  ../include/title.h ../include/addressbook.h \
  ../include/net.h \
  ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/util.h ../include/buf.h \
  ../include/npcutil.h ../include/char_base.h ../include/object.h \
  ../include/char_data.h ../include/handletime.h ../include/chatmagic.h \
  ../include/configfile.h ../include/readmap.h ../include/map_deal.h \
  ../include/lssproto_serv.h ../include/lssproto_util.h \
  ../include/log.h ../include/battle.h \
  ../include/pet.h ../include/enemy.h ../include/encount.h \
  ../include/magic_base.h ../include/magic.h ../include/pet_skill.h \
  ../include/pet_event.h ../include/item_gen.h \
  ../include/npc_eventaction.h ../include/map_warppoint.h \
  ../include/npc_manorsman.h ../include/net.h ../include/saacproto_cli.h \
  ../include/saacproto_util.h ../include/npc_scheduleman.h \
  ../include/trade.h ../include/npccreate.h ../include/char_talk.h \
  ../include/family.h ../include/petmail.h ../include/npc_autopk.h \
  ../include/item.h
event.o: event.c ../include/version.h ../include/correct_bug.h \
  ../include/object.h ../include/common.h \
  ../include/char_base.h \
  ../include/version.h ../include/skill.h ../include/util.h \
  ../include/title.h ../include/addressbook.h \
  ../include/net.h \
  ../include/char.h ../include/char_base.h \
  ../include/char_data.h ../include/item.h ../include/char.h \
  ../include/readmap.h ../include/map_warppoint.h ../include/event.h \
  ../include/npc_warp.h ../include/npc_npcenemy.h
char_walk.o: char_walk.c ../include/version.h ../include/correct_bug.h \
  ../include/common.h \
  ../include/handletime.h \
  ../include/common.h \
  ../include/object.h ../include/char_base.h ../include/version.h \
  ../include/skill.h ../include/util.h \
  ../include/title.h \
  ../include/addressbook.h ../include/net.h \
  ../include/char.h \
  ../include/char_base.h ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/char_event.h ../include/lssproto_serv.h \
  ../include/lssproto_util.h \
  ../include/readmap.h \
  ../include/map_deal.h ../include/npccreate.h ../include/encount.h \
  ../include/npcutil.h ../include/battle.h ../include/net.h \
  ../include/configfile.h ../include/npc_npcenemy.h
encount.o: encount.c ../include/version.h ../include/correct_bug.h \
  ../include/common.h \
  ../include/util.h \
  ../include/common.h ../include/buf.h \
  ../include/char_base.h ../include/version.h ../include/skill.h \
  ../include/util.h ../include/title.h ../include/addressbook.h \
  ../include/net.h \
  ../include/char.h ../include/char_base.h \
  ../include/char_data.h ../include/item.h ../include/char.h \
  ../include/configfile.h ../include/encount.h ../include/enemy.h
pet.o: pet.c ../include/version.h ../include/correct_bug.h \
  ../include/char_base.h ../include/version.h \
  ../include/skill.h ../include/common.h \
  ../include/util.h \
  ../include/title.h ../include/addressbook.h \
  ../include/net.h \
  ../include/char.h ../include/char_base.h \
  ../include/char_data.h ../include/item.h ../include/char.h \
  ../include/object.h ../include/readmap.h ../include/map_deal.h \
  ../include/lssproto_serv.h ../include/lssproto_util.h \
  ../include/handletime.h ../include/pet.h ../include/battle.h \
  ../include/petmail.h ../include/log.h ../include/function.h
enemy.o: enemy.c ../include/version.h ../include/correct_bug.h \
  ../include/common.h \
  ../include/util.h \
  ../include/common.h ../include/buf.h \
  ../include/char_base.h ../include/version.h ../include/skill.h \
  ../include/util.h ../include/title.h ../include/addressbook.h \
  ../include/net.h \
  ../include/char.h ../include/char_base.h \
  ../include/char_data.h ../include/item.h ../include/char.h \
  ../include/configfile.h ../include/encount.h ../include/enemy.h \
  ../include/pet.h ../include/enemyexptbl.h ../include/petmail.h \
  ../include/battle.h ../include/pet_skillinfo.h ../include/anim_tbl.h \
  ../include/log.h ../include/npcutil.h
pet_event.o: pet_event.c ../include/version.h ../include/correct_bug.h \
  ../include/common.h \
  ../include/object.h \
  ../include/common.h ../include/char_base.h ../include/version.h \
  ../include/skill.h ../include/util.h \
  ../include/title.h ../include/addressbook.h ../include/net.h \
  ../include/char.h ../include/char_base.h \
  ../include/char_data.h ../include/item.h ../include/char.h \
  ../include/configfile.h ../include/handletime.h ../include/pet_event.h \
  ../include/npcutil.h ../include/log.h ../include/lssproto_serv.h \
  ../include/lssproto_util.h \
  ../include/npc_exchangeman.h ../include/npc_eventaction.h
char_talk.o: char_talk.c ../include/version.h ../include/correct_bug.h \
  ../include/readmap.h ../include/common.h \
  ../include/util.h \
  ../include/object.h ../include/char.h \
  ../include/char_base.h ../include/version.h ../include/skill.h \
  ../include/title.h ../include/addressbook.h ../include/net.h \
  ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/char_base.h ../include/chatmagic.h \
  ../include/battle.h ../include/log.h ../include/configfile.h \
  ../include/lssproto_serv.h ../include/lssproto_util.h \
  ../include/saacproto_cli.h \
  ../include/saacproto_util.h ../include/family.h ../include/net.h
char_party.o: char_party.c ../include/version.h ../include/correct_bug.h \
  ../include/readmap.h ../include/common.h \
  ../include/util.h \
  ../include/object.h ../include/char.h \
  ../include/char_base.h ../include/version.h ../include/skill.h \
  ../include/title.h ../include/addressbook.h ../include/net.h \
  ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/char_base.h ../include/battle.h \
  ../include/lssproto_serv.h ../include/lssproto_util.h \
  ../include/npcutil.h ../include/npc_bus.h ../include/npc_airplane.h \
  ../include/family.h ../include/init.h
char_item.o: char_item.c ../include/version.h ../include/correct_bug.h \
  ../include/configfile.h ../include/common.h \
  ../include/readmap.h \
  ../include/util.h \
  ../include/map_deal.h ../include/object.h \
  ../include/char.h ../include/char_base.h ../include/version.h \
  ../include/skill.h ../include/title.h ../include/addressbook.h \
  ../include/net.h \
  ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/char_base.h ../include/item.h \
  ../include/lssproto_serv.h ../include/lssproto_util.h \
  ../include/handletime.h ../include/log.h ../include/item_event.h \
  ../include/battle.h ../include/petmail.h
petmail.o: petmail.c ../include/version.h ../include/correct_bug.h \
  ../include/configfile.h ../include/common.h \
  ../include/buf.h \
  ../include/char_base.h ../include/version.h ../include/skill.h \
  ../include/util.h \
  ../include/title.h ../include/addressbook.h \
  ../include/net.h \
  ../include/char.h ../include/char_base.h \
  ../include/char_data.h ../include/item.h ../include/char.h \
  ../include/battle.h ../include/handletime.h ../include/map_deal.h \
  ../include/addressbook.h ../include/lssproto_serv.h \
  ../include/lssproto_util.h \
  ../include/pet.h \
  ../include/petmail.h ../include/npcutil.h ../include/log.h
trade.o: trade.c ../include/version.h ../include/correct_bug.h \
  ../include/correct_bug.h \
  ../include/readmap.h \
  ../include/common.h \
  ../include/util.h \
  ../include/object.h ../include/char.h \
  ../include/char_base.h ../include/version.h ../include/skill.h \
  ../include/title.h ../include/addressbook.h ../include/net.h \
  ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/char_base.h ../include/lssproto_serv.h \
  ../include/lssproto_util.h \
  ../include/npcutil.h \
  ../include/trade.h ../include/log.h ../include/handletime.h \
  ../include/buf.h ../include/net.h ../include/battle.h \
  ../include/npc_bus.h ../include/char_talk.h
family.o: family.c ../include/version.h ../include/correct_bug.h \
  ../include/readmap.h ../include/common.h \
  ../include/util.h \
  ../include/object.h ../include/char.h \
  ../include/char_base.h ../include/version.h ../include/skill.h \
  ../include/title.h ../include/addressbook.h ../include/net.h \
  ../include/char_data.h ../include/item.h \
  ../include/char.h ../include/char_base.h ../include/lssproto_serv.h \
  ../include/lssproto_util.h \
  ../include/saacproto_cli.h ../include/saacproto_util.h \
  ../include/npcutil.h ../include/family.h ../include/log.h \
  ../include/handletime.h ../include/buf.h ../include/net.h \
  ../include/battle.h ../include/npc_bus.h ../include/char_talk.h \
  ../include/npc_scheduleman.h ../include/npc_fmdengon.h
