# Molecule testing

Create a new role with molecule

	molecule init role myrole

with galaxy

	ansible-galaxy role init myrole


*creates structure*

`/myrole/molecule/default/` has default testing scenario (envs, usage)

Then test it

	cd myrole
	molecule test

And test it but leave the container running for debugging

	molecule converge

Set a 'breakpoint' using `fail:` in the tasks