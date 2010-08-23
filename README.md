gen_server2 - a copy of LSHIFT's gen_server modifications
=========================================================

_gen_server2_ is a modified version of OTP's gen_server behaviour. 
This repository is hosted so people don't have to keep copying the 
gen_server2 source file into their projects, which is pointless unless
you're planning on making modifications of your own. 

Installation
------------

Using [epm](http://github.com/JacobVorreuter/epm), you can install in the following manner: 

	t4@malachi:~ $ epm install hyperthunk/gen_server2
	epm v0.1.1, 2010

	===============================
	Install the following packages?
	===============================
	    + hyperthunk-gen_server2-master

	([y]/n) y

	+ downloading http://github.com/hyperthunk/gen_server2/tarball/master
	+ compiling with rebar...
	+ running gen_server2 build command
	+ running gen_server2 install command

	t4@malachi:~ $ erl
	Erlang R13B04 (erts-5.7.5) [source] [smp:2:2] [rq:2] [async-threads:0] [hipe] [kernel-poll:false]

	Eshell V5.7.5  (abort with ^G)
	1> code:which(gen_server2).
	"/Users/t4/Library/Erlang/Site/gen_server2-1.0.0/ebin/gen_server2.beam"
	2> 
	
If you're using [rebar](http://github.com/basho/rebar) as your build tool, then you can include this in your dependencies to have
it pulled down automatically: 

	%% file: rebar.config
	{deps, [
	  {gen_server2, "1.0.0", {git, "http://github.com/hyperthunk/gen_server2.git", "master"}}
	]}.

And pull it with get/check-deps:

	t4@malachi:plumber $ rebar get-deps
	==> plumber (get-deps)
	Pulling gen_server2 from {git,"http://github.com/hyperthunk/gen_server2.git",
	                              "master"}
	Initialized empty Git repository in /Users/t4/work/mine/plumber/deps/gen_server2/.git/
	Already on 'master'
	==> gen_server2 (get-deps)
	t4@malachi:plumber $ rebar check-deps
	==> gen_server2 (check-deps)
	==> plumber (check-deps)
	t4@malachi:plumber $


