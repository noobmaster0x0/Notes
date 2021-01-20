#cclang  - CPPCHECK + CLANG

Uma forma simples de chamar o cppcheck e o clang a partir da linha de comando enquanto está compilando algo. Basta adiconar em seu .bashrc
```bash
cclang()
{
	cppcheck --enable=all --platform=native --template="{file}  {line}  {severity} {id}: {message}" --verbose "${1}" ; echo -e "\n\n[+]Tentando compilar mesmo assim\n" ; clang  -W "${@}"
}
```

