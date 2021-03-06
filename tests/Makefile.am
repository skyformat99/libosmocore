AM_CPPFLAGS = -I$(top_srcdir)/include -I$(top_builddir)/include
AM_CFLAGS = -Wall $(TALLOC_CFLAGS)
AM_LDFLAGS =
LDADD = $(top_builddir)/src/libosmocore.la $(TALLOC_LIBS)

if ENABLE_SERCOM_STUB
noinst_LIBRARIES = libsercomstub.a
LDADD += $(top_builddir)/tests/libsercomstub.a
endif

check_PROGRAMS = timer/timer_test sms/sms_test ussd/ussd_test		\
                 smscb/smscb_test bits/bitrev_test a5/a5_test		\
                 conv/conv_test auth/milenage_test lapd/lapd_test	\
                 gsm0808/gsm0808_test gsm0408/gsm0408_test		\
		 gprs/gprs_test	kasumi/kasumi_test gea/gea_test		\
		 logging/logging_test codec/codec_test			\
		 loggingrb/loggingrb_test strrb/strrb_test              \
		 comp128/comp128_test smscb/gsm0341_test		\
		 bitvec/bitvec_test msgb/msgb_test bits/bitcomp_test	\
		 bits/bitfield_test					\
		 tlv/tlv_test gsup/gsup_test oap/oap_test		\
		 write_queue/wqueue_test socket/socket_test		\
		 coding/coding_test conv/conv_gsm0503_test		\
		 abis/abis_test endian/endian_test sercomm/sercomm_test	\
		 prbs/prbs_test gsm23003/gsm23003_test 			\
		 codec/codec_ecu_fr_test timer/clk_override_test

if ENABLE_MSGFILE
check_PROGRAMS += msgfile/msgfile_test
endif

if ENABLE_PCSC
check_PROGRAMS += sim/sim_test
endif

if ENABLE_UTILITIES
check_PROGRAMS += utils/utils_test
endif

if ENABLE_VTY
check_PROGRAMS += vty/vty_test
endif

if ENABLE_CTRL
check_PROGRAMS += ctrl/ctrl_test fsm/fsm_test
endif

if ENABLE_STATS_TEST
check_PROGRAMS += stats/stats_test
endif

if ENABLE_GB
check_PROGRAMS += gb/bssgp_fc_test gb/gprs_bssgp_test gb/gprs_ns_test fr/fr_test
endif

utils_utils_test_SOURCES = utils/utils_test.c
utils_utils_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

stats_stats_test_SOURCES = stats/stats_test.c
stats_stats_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

a5_a5_test_SOURCES = a5/a5_test.c
a5_a5_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libgsmint.la

kasumi_kasumi_test_SOURCES = kasumi/kasumi_test.c
kasumi_kasumi_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libgsmint.la

comp128_comp128_test_SOURCES = comp128/comp128_test.c
comp128_comp128_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

auth_milenage_test_SOURCES = auth/milenage_test.c
auth_milenage_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

abis_abis_test_SOURCES = abis/abis_test.c
abis_abis_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

ctrl_ctrl_test_SOURCES = ctrl/ctrl_test.c
ctrl_ctrl_test_LDADD = $(LDADD) $(top_builddir)/src/ctrl/libosmoctrl.la

gea_gea_test_SOURCES = gea/gea_test.c
gea_gea_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

bits_bitrev_test_SOURCES = bits/bitrev_test.c

bitvec_bitvec_test_SOURCES = bitvec/bitvec_test.c

bits_bitcomp_test_SOURCES = bits/bitcomp_test.c

bits_bitfield_test_SOURCES = bits/bitfield_test.c

conv_conv_test_SOURCES = conv/conv_test.c conv/conv.c
conv_conv_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libgsmint.la

conv_conv_gsm0503_test_SOURCES = conv/conv_gsm0503_test.c conv/conv.c conv/gsm0503_test_vectors.c
conv_conv_gsm0503_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libgsmint.la
conv_conv_gsm0503_test_CPPFLAGS = $(AM_CPPFLAGS) -I$(top_srcdir)/tests/conv

gsm0808_gsm0808_test_SOURCES = gsm0808/gsm0808_test.c
gsm0808_gsm0808_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

gsm0408_gsm0408_test_SOURCES = gsm0408/gsm0408_test.c
gsm0408_gsm0408_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

gprs_gprs_test_SOURCES = gprs/gprs_test.c
gprs_gprs_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

lapd_lapd_test_SOURCES = lapd/lapd_test.c
lapd_lapd_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

msgb_msgb_test_SOURCES = msgb/msgb_test.c

msgfile_msgfile_test_SOURCES = msgfile/msgfile_test.c

smscb_smscb_test_SOURCES = smscb/smscb_test.c
smscb_smscb_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

smscb_gsm0341_test_SOURCES = smscb/gsm0341_test.c
smscb_gsm0341_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

sms_sms_test_SOURCES = sms/sms_test.c
sms_sms_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

timer_timer_test_SOURCES = timer/timer_test.c

timer_clk_override_test_SOURCES = timer/clk_override_test.c

ussd_ussd_test_SOURCES = ussd/ussd_test.c
ussd_ussd_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

gb_bssgp_fc_test_SOURCES = gb/bssgp_fc_test.c
gb_bssgp_fc_test_LDADD = $(LDADD) $(top_builddir)/src/gb/libosmogb.la \
			 $(top_builddir)/src/gsm/libosmogsm.la

gb_gprs_bssgp_test_SOURCES = gb/gprs_bssgp_test.c
gb_gprs_bssgp_test_LDADD = $(LDADD) $(top_builddir)/src/gb/libosmogb.la $(LIBRARY_DLSYM) \
			   $(top_builddir)/src/gsm/libosmogsm.la

gb_gprs_ns_test_SOURCES = gb/gprs_ns_test.c
gb_gprs_ns_test_LDADD = $(LDADD) $(top_builddir)/src/gb/libosmogb.la $(LIBRARY_DLSYM) \
			$(top_builddir)/src/gsm/libosmogsm.la

logging_logging_test_SOURCES = logging/logging_test.c

fr_fr_test_SOURCES = fr/fr_test.c
fr_fr_test_LDADD = $(LDADD) $(top_builddir)/src/gb/libosmogb.la $(LIBRARY_DLSYM) \
		   $(top_builddir)/src/gsm/libosmogsm.la

codec_codec_test_SOURCES = codec/codec_test.c
codec_codec_test_LDADD = $(LDADD) $(top_builddir)/src/codec/libosmocodec.la

codec_codec_ecu_fr_test_SOURCES = codec/codec_ecu_fr_test.c
codec_codec_ecu_fr_test_LDADD = $(LDADD) $(top_builddir)/src/codec/libosmocodec.la

loggingrb_loggingrb_test_SOURCES = loggingrb/loggingrb_test.c
loggingrb_loggingrb_test_LDADD = $(LDADD)

strrb_strrb_test_SOURCES = strrb/strrb_test.c

vty_vty_test_SOURCES = vty/vty_test.c
vty_vty_test_LDADD = $(LDADD) $(top_builddir)/src/vty/libosmovty.la

sim_sim_test_SOURCES = sim/sim_test.c
sim_sim_test_LDADD = $(LDADD) $(top_builddir)/src/sim/libosmosim.la \
		     $(top_builddir)/src/gsm/libosmogsm.la

tlv_tlv_test_SOURCES = tlv/tlv_test.c
tlv_tlv_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

gsup_gsup_test_SOURCES = gsup/gsup_test.c
gsup_gsup_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

oap_oap_test_SOURCES = oap/oap_test.c
oap_oap_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

fsm_fsm_test_SOURCES = fsm/fsm_test.c
fsm_fsm_test_LDADD = $(LDADD) $(top_builddir)/src/ctrl/libosmoctrl.la

write_queue_wqueue_test_SOURCES = write_queue/wqueue_test.c

socket_socket_test_SOURCES = socket/socket_test.c

coding_coding_test_SOURCES = coding/coding_test.c
coding_coding_test_LDADD = $(LDADD) \
  $(top_builddir)/src/gsm/libosmogsm.la \
  $(top_builddir)/src/codec/libosmocodec.la \
  $(top_builddir)/src/coding/libosmocoding.la

endian_endian_test_SOURCES = endian/endian_test.c

sercomm_sercomm_test_SOURCES = sercomm/sercomm_test.c

prbs_prbs_test_SOURCES = prbs/prbs_test.c

gsm23003_gsm23003_test_SOURCES = gsm23003/gsm23003_test.c
gsm23003_gsm23003_test_LDADD = $(LDADD) $(top_builddir)/src/gsm/libosmogsm.la

# The `:;' works around a Bash 3.2 bug when the output is not writeable.
$(srcdir)/package.m4: $(top_srcdir)/configure.ac
	:;{ \
               echo '# Signature of the current package.' && \
               echo 'm4_define([AT_PACKAGE_NAME],' && \
               echo '  [$(PACKAGE_NAME)])' && \
               echo 'm4_define([AT_PACKAGE_TARNAME],' && \
               echo '  [$(PACKAGE_TARNAME)])' && \
               echo 'm4_define([AT_PACKAGE_VERSION],' && \
               echo '  [$(PACKAGE_VERSION)])' && \
               echo 'm4_define([AT_PACKAGE_STRING],' && \
               echo '  [$(PACKAGE_STRING)])' && \
               echo 'm4_define([AT_PACKAGE_BUGREPORT],' && \
               echo '  [$(PACKAGE_BUGREPORT)])'; \
               echo 'm4_define([AT_PACKAGE_URL],' && \
               echo '  [$(PACKAGE_URL)])'; \
             } >'$(srcdir)/package.m4'

EXTRA_DIST = testsuite.at $(srcdir)/package.m4 $(TESTSUITE)		\
             timer/timer_test.ok sms/sms_test.ok ussd/ussd_test.ok	\
             smscb/smscb_test.ok bits/bitrev_test.ok a5/a5_test.ok	\
             conv/conv_test.ok auth/milenage_test.ok ctrl/ctrl_test.ok	\
             lapd/lapd_test.ok gsm0408/gsm0408_test.ok			\
             gsm0808/gsm0808_test.ok gb/bssgp_fc_tests.err		\
             gb/bssgp_fc_tests.ok gb/bssgp_fc_tests.sh			\
             gb/gprs_bssgp_test.ok gb/gprs_ns_test.ok gea/gea_test.ok	\
             gprs/gprs_test.ok kasumi/kasumi_test.ok			\
             msgfile/msgfile_test.ok msgfile/msgconfig.cfg		\
             logging/logging_test.ok logging/logging_test.err		\
             fr/fr_test.ok loggingrb/logging_test.ok			\
             loggingrb/logging_test.err	strrb/strrb_test.ok		\
             codec/codec_test.ok \
             codec/codec_ecu_fr_test.ok \
	     vty/vty_test.ok \
	     vty/fail_not_de-indented.cfg \
	     vty/fail_tabs_and_spaces.cfg \
	     vty/fail_too_much_indent.cfg \
	     vty/ok.cfg \
	     vty/ok_empty_parent.cfg \
	     vty/ok_ignore_blank.cfg \
	     vty/ok_ignore_comment.cfg \
	     vty/ok_indented_root.cfg \
	     vty/ok_more_spaces.cfg \
	     vty/ok_tabs_and_spaces.cfg \
	     vty/ok_tabs.cfg \
	     comp128/comp128_test.ok bits/bitfield_test.ok		\
	     utils/utils_test.ok stats/stats_test.ok			\
	     bitvec/bitvec_test.ok msgb/msgb_test.ok bits/bitcomp_test.ok \
	     sim/sim_test.ok tlv/tlv_test.ok abis/abis_test.ok		\
	     gsup/gsup_test.ok gsup/gsup_test.err			\
	     oap/oap_test.ok fsm/fsm_test.ok fsm/fsm_test.err		\
	     write_queue/wqueue_test.ok socket/socket_test.ok		\
	     socket/socket_test.err coding/coding_test.ok		\
	     osmo-auc-gen/osmo-auc-gen_test.sh				\
	     osmo-auc-gen/osmo-auc-gen_test.ok				\
	     osmo-auc-gen/osmo-auc-gen_test.err				\
	     conv/conv_gsm0503_test.ok endian/endian_test.ok 		\
	     sercomm/sercomm_test.ok prbs/prbs_test.ok			\
	     gsm23003/gsm23003_test.ok                                 \
	     timer/clk_override_test.ok

DISTCLEANFILES = atconfig atlocal conv/gsm0503_test_vectors.c
BUILT_SOURCES = conv/gsm0503_test_vectors.c
noinst_HEADERS = conv/conv.h

TESTSUITE = $(srcdir)/testsuite

check-local: atconfig $(TESTSUITE)
	cat /proc/cpuinfo
	$(SHELL) '$(TESTSUITE)' $(TESTSUITEFLAGS)

installcheck-local: atconfig $(TESTSUITE)
	$(SHELL) '$(TESTSUITE)' AUTOTEST_PATH='$(bindir)' \
		$(TESTSUITEFLAGS)

clean-local:
	test ! -f '$(TESTSUITE)' || \
		$(SHELL) '$(TESTSUITE)' --clean

AUTOM4TE = $(SHELL) $(top_srcdir)/missing --run autom4te
AUTOTEST = $(AUTOM4TE) --language=autotest
$(TESTSUITE): $(srcdir)/testsuite.at $(srcdir)/package.m4
	$(AUTOTEST) -I '$(srcdir)' -o $@.tmp $@.at
	mv $@.tmp $@

conv/gsm0503_test_vectors.c: $(top_srcdir)/utils/conv_gen.py $(top_srcdir)/utils/conv_codes_gsm.py
	$(AM_V_GEN)python $(top_srcdir)/utils/conv_gen.py gen_vectors gsm \
		--target-path $(builddir)/conv
