# FSL-skull-stripping
Script to strip skulls (a.k.a extract brain) in anatomical image

strip_skulls.sh:
 - Strips skull/non-brain matter from anatomical image
 - Adjust the FIT parameter which controls how much matter gets stripped; you may want to record this value somewhere
 - After running script, inspect each subject's anatomical image in fslview to ensure no loss of PFC (too much stripped) or excess dura around brain (too little stripped), then adjust FIT parameter as needed and re-run script until you like the results
 - It may be easiest to first run all subjects with a ballpark FIT parameter (~0.3), then tweak it for each subject individually as needed
 - To run batches of subjects, submit as job using mksub jobs/strip_skulls.pbs
 - Discovery can handle all subjects in one job
