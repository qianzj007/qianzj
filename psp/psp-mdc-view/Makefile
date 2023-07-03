install:
	for i in `ls | grep -v Makefile`;do helm install -n $(env) -f $$i/$(env)-values.yaml $$i $$i/;done

uninstall:
	for i in `helm list -n $(env) | grep -v NAME | awk '{print $$1}'`;do helm uninstall $$i -n $(env) ;done
