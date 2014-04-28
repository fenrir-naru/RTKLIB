# Minimal RTKLIB for embedded computing.
================

[![Build Status](https://travis-ci.org/fenrir-naru/RTKLIB.svg?branch=spike)](https://travis-ci.org/fenrir-naru/RTKLIB)

This software is originated from RTKLIB, which is An Open Source Program Package for GNSS Positioning written by T. Takasu, and modified by M. Naruoka to fit for embedded computing.
The major differences are the following:

1. Runnable without file.
2. Runnable without thread.
3. Runnable without system header such as providing time functions.
4. Runnable with smaller memory.

Please see [minimal_rtkpos](fenrir-naru/RTKLIB/tree/spike/app/minimal_rtkpos) for ppp-positioning, 
and [minimal_pntpos](fenrir-naru/RTKLIB/tree/spike/app/minimal_pntpos) for single-positioning. 

The license of this software follows one of RTKLIB, that is, so-called BSD 2-clause license.

--------------------------------------------------------------------------------

LICENSE

The minimal RTKLIB software package is distributed under the following BSD 
2-clause license (http://opensource.org/licenses/BSD-2-Clause) and 
additional an exclusive clauses. Users are permitted to develop, 
produce or sell their own non-commercial or commercial products utilizing, 
linking or including minimal RTKLIB as long as they comply with the license.

          Copyright (c) 2007-2013, T. Takasu, All rights reserved
          for the original RTKLIB.

Also,
          Copyright (c) 2014-, M. Naruoka, All rights reserved
          for the differences between the minimal and the original RTKLIB.  

Redistribution and use in source and binary forms, with or without modification,
are permitted provided that the following conditions are met:

- Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

- Redistributions in binary form must reproduce the above copyright notice, this
  list of conditions and the following disclaimer in the documentation and/or
  other materials provided with the distribution.

- The software package includes some companion executive binaries or shared
  libraries necessary to execute APs on Windows. These licenses succeed to the
  original ones of these software. 

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE
GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF
THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

--------------------------------------------------------------------------------
