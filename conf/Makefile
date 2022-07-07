#-------------------------------------------------------------------------
#
#  Copyright (c) 2021 Rajit Manohar
#
#  Licensed under the Apache License, Version 2.0 (the "License");
#  you may not use this file except in compliance with the License.
#  You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
#  Unless required by applicable law or agreed to in writing, software
#  distributed under the License is distributed on an "AS IS" BASIS,
#  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#  See the License for the specific language governing permissions and
#  limitations under the License.
#  
#-------------------------------------------------------------------------
include $(ACT_HOME)/scripts/Makefile.std

CONFS=actsim.conf \
	layout.conf \
	lint_opts.conf \
	prs2net.conf \
	global.conf \
	lint.conf \
	lvp.conf \
	expropt.conf


install: $(CONFS)
	@echo "Installing configuration for sky130l..."
	@if [ ! -d $(ACT_HOME)/conf/sky130l ]; then mkdir $(ACT_HOME)/conf/sky130l; fi
	@for i in $(CONFS); do $(ACT_HOME)/scripts/install $$i $(ACT_HOME)/conf/sky130l/$$i; done

-include Makefile.deps
