This python script can be used to profile a shell script.

Once the profiler is on the path, call it like so:

	~> profile test-file.sh PARAM1 PARAM2

The output will look something like the following:

	0.291234732	>	/bin/bash	line 7	echo 'loop: 1'
	0.289730072	>	/bin/bash	line 6	for i in '`seq 100`'
	0.006031990	>	/bin/bash	line 5	seq 10
	0.005759716	>>	/bin/bash	line 8	seq 100
	0.003070116	>	/bin/bash	line 9	echo c
	0.003000021	>	/bin/bash	line 4	echo b
	0.002927542	>	/bin/bash	line 3	echo a
	0.002631426	>	/bin/bash	line 2	echo test-file.sh
	0.000000000	>	/bin/bash	line 10	echo --- END OF PROFILING ---
