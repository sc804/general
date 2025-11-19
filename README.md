# general

###################
##    TESTERS    ##
###################

PrintftTester : #Tripouille
	git clone git@github.com:Tripouille/printfTester.git
	cd printfTester && make m
	cd ..
	rm -rf printfTester/

Tester-Santana : #ft_printf_tester
	git clone git@github.com:paulo-santana/ft_printf_tester.git
	cd ft_printf_tester && sh test m
	rm -rf ft_printf_tester

Tester-nmannage :
	curl -o test.c https://raw.githubusercontent.com/nmannage/printftester_mandatory/refs/heads/main/test.c
	make && cc test.c -L. -lftprintf -o test && ./test
	rm -rf test test.c
