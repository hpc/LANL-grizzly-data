ANONYMIZED Grizzly SLURM job logs
	DATE RANGE: January 31, 2018 -> November 19, 2018
	FILE NAME: gr-slurm-logs_anon.gz
	FILE SIZE: 6.6MB gzipped (149MB uncompressed)
	NUMBER OF LINES: 4,358,670
	LANL PUBLIC RELEASE ID: LA-UR-18-30996
	CONTACT: 
		Nathan DeBardeleben 
		ndebard@lanl.gov
		Ultrascale Systems Research Center (USRC)
		High Performance Computing Design (HPC-DES)
		Los Alamos National Laboratory (LANL)
		Los Alamos, NM 87545
	DATE OF RELEASE: November 20, 2018
	DESCRIPTION:
		This data contains output records from the SLURM resource
		manager running jobs on the open compute cluster, Grizzly.
		The account_name, group_name, jobname, and user_name fields
		have been anonymized with a simple integer 1 ->
		max_unique_of_that_field.  The anonymization preserves the data
		such that jobname 'abcd', should it be run repeatedly, will
		always map to the same anonymized jobname (e.g.
		'jobname_1234').  This is true for all of the anonymized
		fields.

		The CONTACT (above) has a mapping from anonymized data back to
		the real data values.  If a researcher finds something
		particularly valuable, LANL may be interested in understanding
		the relationship with the real non-anonymized fields.  Please
		email the CONTACT with these findings.

		The data is a dump of a Python list where each element is
		itself a dictionary.  One such element (the dictionary at that
		element) is as follows:

			{   'account_name': 'account_name_19',
			        'calc_wallclock': '29610360',
			        'cluster': 'grizzly',
			        'dispatch_time': '2018-01-31 09:45:53',
			        'end_state': 'TIMEOUT',
			        'end_time': '2018-01-31 13:46:23',
			        'exit_code': '0:0',
			        'exit_info': '0:0',
			        'exitstatus': '0:0',
			        'group_name': 'group_name_60',
			        'host': 'gr-master',
			        'host_list': 'gr[0145-0201]',
			        'jobid': '15040144',
			        'jobname': 'jobname_8',
			        'num_procs_exe': '2052',
			        'processor_seconds': '29610360',
			        'qos': 'interactive',
			        'queue': 'standard',
			        'req_nodes': '57',
			        'start_time': '2018-01-31 09:45:53',
			        'submit_time': '2018-01-31 09:30:37',
			        'timestamp': '2018-01-31T13:46:23-07:00',
			        'user_name': 'user_name_60',
			        'wallclock_limit': '14400'},

		This entry should be obvious, but one can see that the job
		"jobname_8" ran on 57 nodes of Grizzly - gr145-gr201.  The job
		ended in a TIMEOUT.  The job waited in the queue roughly 5
		minutes before executing.

		The values exit_code, exit_info, and exitstatus may be
		valuable, but it is not entirely clear at this time their
		value.  For instance, some jobs that have end_state FAILED have
		these values:

		        'exit_code': '2:0',
			'exit_info': '0:0',
			'exitstatus': '2:0',

			'exit_code': '1:0',
			'exit_info': '0:0',
			'exitstatus': '1:0',

		A quick glance shows that other values for these keys are
		present in the log for other job end states as well.  These
		values may be usable or may not be.

	INFORMATION ABOUT GRIZZLY:
		Grizzly is a CTS-1 system at LANL.  
		It runs the TOSS operating stack.  
		It became available to users January 20, 2017.  
		At the time of this data release, Grizzly is still in operation.
		Grizzly has 8 SUs plus 18 additional compute nodes. The SU is a
			building block concept described in detail at the CTS-1
			architecture description.  
		Grizzly has 32 I/O Nodes.  
		The total number of compute nodes is: 1490 (i.e. 184*8 + 18 
			additional).
		Grizzly has 181TB of main memory DRAM (DDR).

		At the time of writing this, the Grizzly cluster's top500.org
		entry can be found here:
			https://www.top500.org/system/178972

