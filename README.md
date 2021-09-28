

@@ -1,5 +1,125 @@
#!/bin/bash
# Deobfus By X - MrG3P5

# Obfuscated By @Gybran21
trap 'store; exit 1;' 2
threads="20"
bl="\033[30;1m"
r="\033[31;1m"
y="\033[33;1m"
yl="\033[1;33m"
g="\033[0;32m"
gl="\033[32;1m"
b="\033[0;36m"
c="\033[36;1m"
p="\033[0;35m"
o="\033[0m"
cek(){
command -v wget > /dev/null 2>&1 || { echo >&2 "wget belum terinstall ketik >> pkg install wget -y .....lalu ketik bash empas"; exit 1; }
command -v pv > /dev/null 2>&1 || { echo >&2 "pv belum terinstall ketik >> pkg install pv -y .....lalu ketik bash empas"; exit 1; }
}
banner(){
clear
echo -e "" | pv -qL 600
echo -e "" | pv -qL 600
echo -e "$yl          _______$bl _______  _____  _______ _______" | pv -qL 600
echo -e "$yl          |______$bl |  |  | |_____] |_____| |______" | pv -qL 600
echo -e "$yl          |______$bl |  |  | |       |     | ______|" | pv -qL 600
echo -e "" | pv -qL 600
echo -e "$bl        -----------------$yl Project $bl----------------" | pv -qL 600
echo -e "$yl             Youtube : Fahmi Cog" | pv -qL 600
echo -e "$yl             Github  : github.com/fahmicog" | pv -qL 600
echo -e "$bl        ------------------------------------------" | pv -qL 600
echo -e ""
}

vmMIUaVlXLVRsSyBMBkOWGxaLanrSoZMoVtjXDtbthkFdqyueRzgTprDSGgTqiWdfKTRMazLdoBefWCvqQgAQzxELPIEVBgnPLWK="HTEzVgcEmjYQNkPCAiLTEQiMnIBJtrUyLipqMMInFFKexdDOARHNfwrjpdShqwydCTHOTDOtUVnqhEVheEPVsHSvAMOZIFhFKpWA";WKhgRCyhBecAirmjtAIwIQRjtgCAxrjwGNZDlEhnidfkQZQIwskPCxvQngsfVCRTDdFQNLhlzdPcbaFEENsePhWJSxcKuzjiOhgH="tauwozwBmfUGfltidjSYyqEWodpAOCzriPvsTyioGsyhLkyuKCMRXpkdIIJKrprivUGivhBHyiQzcfTUywNTbfhHfZhxSQuUerpR";pgfiQPOBlfdXTWRFlzNFRouRxVGOxaOnGCRACsACDpWLjScGVaxsqJdYiWUTAhzQIDBDHggwRfsJkZaIhVLTlmQJgLePeTZpBKOX="ch";KbbAcswXIuupeLReFCkERetbagDPOxNocCIJnTpJmleEynVEjwDCFNOwRimIBjBOfWaUeVThmevaJBQGVLpdHPsxkmRgvsZvHpnt="4";iGcuhEeSlqMLuAyGBUjoCWLaNfqgSoMOdghCqnnohzflCSGGybSGoPdtCXOiauUPwsaWAmrBvvmjVaKexiGBLNzMXWEDAybyHksO="";cYkKIzmCLvtcqFOMUPQxVKQZxuPcCeOjEuTAExXVkJrCGoBtwuKcacxOTQMScFGomYZfCFLSUjTWpTSvkhJiyggpooDzbIdvojGr="SNJWCygMQvjUDZhRyraOphMxNSCNyMPmaszMZNKQDqGkAAxEPzsHkjKWUJdggUroQKcsvXKjZskwRFJeKBNSkAhqjFNnMxyAEavo";RSAybSoiSOXeuGjrQQltJoGYmVOOPOwHFkjGxUpWselATlfPSNpcKBSAniHghgTHDKGvHcRjzQbulhekwwAtZZJtUKXubBGpPDEk=" =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 | r";KcFcSzspZWEFFjuhqtmXeDGtdyCOmYnMlCQjBAOhayCYRlzZMuXAIwmudpMcFuueNeziRMDRUxwlHbjMVXohRJhDKstFxTEUTNYS="cQAwlCeqvFjFfUkflZmjyaXiFzdeVHNBmlgGLZCxAhygzhfGpmWFdzNnkXgKwSRLgWRxgjswOZTbjNeKXedKgpeenHDSIizjUkBV";auZWrgVzbMuNBltnNtOuwhtLGLeEqwRUsklPiBQvJXPVwThVaFIRqRiFWeDdViRrCvBdMrtfmrbmXDNBXIwUQzYRqMpgOrZssUzs="";SrDCyKTPxodwxVRYedoDAxAkLkkvayjyEdfPlmTNgglIuepaphwJNfXOEPtEPcZtQhAeIZOSeMUkDrSYuVzrclqANmKcMCKyARci="as";pQIuoNoOfIYAhfJUHmgwBwdFexNdpkmXrtUwVxAYlyXHIvDBJpeAAGZjEYdFDcWbRokMLbOpIaoYKdzPSnGsfifpRhoZYZiVoACp="ujJTnZPGVFETXwYNJZtAYRuSwaTcnmJoyMKoiXAcdErDCAoIhuMlETzbvylrySlMZXKbPWCyRinGNBSKNaSkEUzINSTgNlxcGjzZ";dVmVbvANllKCxHxNBTdxpHnqbqsMNfGdAGBjfgLkzTOirPjMDRFqcQroOgAgIdxlTeGDYUoXcKdVjofyowDPtDbMswjXuNsNQaBL="KmzGpLLqbFywNaFGEMGPHrLGIfxAtZKrqtJtcsdjnuQlilRMjshmpJFnRUOxvBndZxHLEXxCNFerzokHuiVYtnhSWncrEmOSSRzr";pedRFnzPCQHPyGzposNXBOaElEPLJcWMbUZjxKWMxPtQRmywQQBpqaZgaceCmhfPQSTLIJNSkIETBQVSDgxZtSaTPooGmoUcwEyI="o";OOlFzvHZQFdNfNdEezGRDfCXXaBmBndXGVzcmqwdenrPDeQPhxqkFeMCVouBpwPuiIaIFTneLjUBxaRTWtujuifGtYzNfuIVhNtr="6";bWmJvNXAhADHpGTFCCSQcRaSixvugdfeBoQCfkBZXAqowZGapIkhgzkckbeywvRousvcPWiPKQVGVTAQFHcgFVTLPFsVLCpxsTUx="khoOtRyHdqHTFSdItuanOarmIICcdUUUTNzyhGWGuNWrEFhAfWRexDNvPngrAVRpReUgnTvfOtqHldspAWnVpmgfTLCaafBcaFpG";diYgxqFenujwtCsYZGNAIKRuvAOdYXZcTZyPGmpEgukDlJzSRWWPmuNnphdWQCgYJhcyFkGupiRuaETlleUGdqLzhPEIwdvYQNwC=" -d";cOpqIJciebfXtaTcANguuvVapArKvMGLvwkFLxqMHabdxsdlXcbtvAAwCShXcPkjPKqGTlMJZIzCmcRVpLWMeFpMzeLZWtaRXueg="AzaiNtzQCnTWugfDJpZJQLYUVwwOIPaFdoeLRsyAbBpeyQAKTqwHaslMIwzahxddOuuaUXBePlWWKEzddIxseBwVREIZcySAJZAz";FPsvlRDyxQXGLzScxdNbpqxrPaEoLeyNfReRkcsjvUISVKaRgZRLsyCmjrBtWPTSWyrfCYqRMeexnaTOPMTwaICKitdevkmQwdfB="";HkYbDrBzMBVVhBFYlZAqIuFDGTRESvoxjdDzSTtayneXqnXdNZDBtfmSWbVtZeRiXGcFRERMnyCaoxJQGqelvlwPQLZliBmDIrsZ="b";qIsZBYVWCHSOKmPwtgCcrZCKZAbMqrpXBTDYbnDTzhvimYsCoXoSZrZcfArKpJRIroIyiDzJKFaHiLCiLMizRbDvsFUlugQTXYJV="e";QfFVeuvWSlwXpKSKPTReVOWaDCjYEWwRTTQKUpFjfXVCSWSOJBCFVHRkQsBWGwurFvXOjqIfNJIuXMkWgQrgiRaOrCbdBzCUqQqA="v |";Tx=Eds;UmmFwlsuWHwzLMDGEgaCsRqGzoFXOJVpjjUqKmxxWEIjdsZtieheigRjICeqRlLKesWqZELCTMFmPLrOlWTvmBfoxtiKSQHvXaIr="";NmIbLUGbMGUNqXMjRttQLbcWLDBgEQvEhNDmEQzcMnTkOEogRUDWMtHsOeZLlummDUKIIcVxFJcyBgZNfMVJEClNIIZMgyWRSuwT=$(eval "$auZWrgVzbMuNBltnNtOuwhtLGLeEqwRUsklPiBQvJXPVwThVaFIRqRiFWeDdViRrCvBdMrtfmrbmXDNBXIwUQzYRqMpgOrZssUzs$qIsZBYVWCHSOKmPwtgCcrZCKZAbMqrpXBTDYbnDTzhvimYsCoXoSZrZcfArKpJRIroIyiDzJKFaHiLCiLMizRbDvsFUlugQTXYJV$pgfiQPOBlfdXTWRFlzNFRouRxVGOxaOnGCRACsACDpWLjScGVaxsqJdYiWUTAhzQIDBDHggwRfsJkZaIhVLTlmQJgLePeTZpBKOX$iGcuhEeSlqMLuAyGBUjoCWLaNfqgSoMOdghCqnnohzflCSGGybSGoPdtCXOiauUPwsaWAmrBvvmjVaKexiGBLNzMXWEDAybyHksO$pedRFnzPCQHPyGzposNXBOaElEPLJcWMbUZjxKWMxPtQRmywQQBpqaZgaceCmhfPQSTLIJNSkIETBQVSDgxZtSaTPooGmoUcwEyI$RSAybSoiSOXeuGjrQQltJoGYmVOOPOwHFkjGxUpWselATlfPSNpcKBSAniHghgTHDKGvHcRjzQbulhekwwAtZZJtUKXubBGpPDEk$qIsZBYVWCHSOKmPwtgCcrZCKZAbMqrpXBTDYbnDTzhvimYsCoXoSZrZcfArKpJRIroIyiDzJKFaHiLCiLMizRbDvsFUlugQTXYJV$QfFVeuvWSlwXpKSKPTReVOWaDCjYEWwRTTQKUpFjfXVCSWSOJBCFVHRkQsBWGwurFvXOjqIfNJIuXMkWgQrgiRaOrCbdBzCUqQqA$auZWrgVzbMuNBltnNtOuwhtLGLeEqwRUsklPiBQvJXPVwThVaFIRqRiFWeDdViRrCvBdMrtfmrbmXDNBXIwUQzYRqMpgOrZssUzs$HkYbDrBzMBVVhBFYlZAqIuFDGTRESvoxjdDzSTtayneXqnXdNZDBtfmSWbVtZeRiXGcFRERMnyCaoxJQGqelvlwPQLZliBmDIrsZ$UmmFwlsuWHwzLMDGEgaCsRqGzoFXOJVpjjUqKmxxWEIjdsZtieheigRjICeqRlLKesWqZELCTMFmPLrOlWTvmBfoxtiKSQHvXaIr$SrDCyKTPxodwxVRYedoDAxAkLkkvayjyEdfPlmTNgglIuepaphwJNfXOEPtEPcZtQhAeIZOSeMUkDrSYuVzrclqANmKcMCKyARci$qIsZBYVWCHSOKmPwtgCcrZCKZAbMqrpXBTDYbnDTzhvimYsCoXoSZrZcfArKpJRIroIyiDzJKFaHiLCiLMizRbDvsFUlugQTXYJV$OOlFzvHZQFdNfNdEezGRDfCXXaBmBndXGVzcmqwdenrPDeQPhxqkFeMCVouBpwPuiIaIFTneLjUBxaRTWtujuifGtYzNfuIVhNtr$iGcuhEeSlqMLuAyGBUjoCWLaNfqgSoMOdghCqnnohzflCSGGybSGoPdtCXOiauUPwsaWAmrBvvmjVaKexiGBLNzMXWEDAybyHksO$KbbAcswXIuupeLReFCkERetbagDPOxNocCIJnTpJmleEynVEjwDCFNOwRimIBjBOfWaUeVThmevaJBQGVLpdHPsxkmRgvsZvHpnt$diYgxqFenujwtCsYZGNAIKRuvAOdYXZcTZyPGmpEgukDlJzSRWWPmuNnphdWQCgYJhcyFkGupiRuaETlleUGdqLzhPEIwdvYQNwC$UmmFwlsuWHwzLMDGEgaCsRqGzoFXOJVpjjUqKmxxWEIjdsZtieheigRjICeqRlLKesWqZELCTMFmPLrOlWTvmBfoxtiKSQHvXaIr");eval "$FPsvlRDyxQXGLzScxdNbpqxrPaEoLeyNfReRkcsjvUISVKaRgZRLsyCmjrBtWPTSWyrfCYqRMeexnaTOPMTwaICKitdevkmQwdfB$NmIbLUGbMGUNqXMjRttQLbcWLDBgEQvEhNDmEQzcMnTkOEogRUDWMtHsOeZLlummDUKIIcVxFJcyBgZNfMVJEClNIIZMgyWRSuwT$auZWrgVzbMuNBltnNtOuwhtLGLeEqwRUsklPiBQvJXPVwThVaFIRqRiFWeDdViRrCvBdMrtfmrbmXDNBXIwUQzYRqMpgOrZssUzs$iGcuhEeSlqMLuAyGBUjoCWLaNfqgSoMOdghCqnnohzflCSGGybSGoPdtCXOiauUPwsaWAmrBvvmjVaKexiGBLNzMXWEDAybyHksO"
mulai (){
wget https://raw.githubusercontent.com/fahmicog/fahmicog/main/BqIoslaA/empas.txt -o done
for anjay in $(shuf empas.txt)
do
echo "$anjay"
sleep 0.3
done
}
empas-fresh (){
wget https://raw.githubusercontent.com/fahmicog/fahmicog/main/BqIoslaA/empas-fresh.txt -o done
for anjayy in $(shuf empas-fresh.txt)
do
echo "$anjayy"
sleep 0.3
done
}
empas-uncheck (){
wget https://raw.githubusercontent.com/fahmicog/fahmicog/main/BqIoslaA/empas-uncheck.txt -o done
for anjayyy in $(shuf empas-uncheck.txt)
do
echo "$anjayyy"
sleep 0.3
done
}
empas-moontod(){
wget https://raw.githubusercontent.com/fahmicog/fahmicog/main/BqIoslaA/empas-monton.txt -o done
for anjayyyy in $(shuf empas-monton.txt)
do
echo "$anjayyyy"
sleep 0.3
done
}
function stor() {
if [[ -n "$threads" ]]; then
printf "\n"
printf "\e[1;91m [*] Waiting threads shutting down...\n\e[0m"
sleep 4
fi
}

function store() {
if [[ -n "$threads" ]]; then
printf "\n"
printf "\e[1;91m [*] Memutuskan program tunggu...\n\e[0m"
rm -rf empass
rm -rf done
rm -rf empas-fresh
rm -rf empas-monton
rm -rf empas-uncheck
sleep 2
echo -e "${g}Selesai${o}"
echo -e "$g╔═╣${y}  Mau lagi gak ? ${g}║"
echo -e "$g║ ╚══════════════════╝"
read -p $'\033[0;32m╚══════>\033[0m ' lagi
if [[ $lagi == 'mau' || $lagi == 'lagi' || $lagi == 'iya' || $lagi == y || $lagi == Y ]]; then
clear
menu
else
exit
fi
fi
}
menu(){
banner
echo -e "    ${bl}(${yl}1${bl})${bl} Update Script${o}" | pv -qL 600
echo -e "    ${bl}(${yl}2${bl})${bl} Langsung Cari Empas${o}" | pv -qL 600
echo -e "    ${bl}(${yl}3${bl})${bl} Langsung Cari Empas Fresh${o}" | pv -qL 600
echo -e "    ${bl}(${yl}4${bl})${bl} Langsung Cari Empas Uncheck${o}" | pv -qL 600
echo -e "    ${bl}(${yl}5${bl})${bl} Langsung Cari Empas Moonton${o}" | pv -qL 600
echo ""
read -p $'  \033[1;33mPilih\033[1;30m?\033[0m ' pilihan
echo ""
if [[ $pilihan == 1 ]]; then
git pull origin master
exit
elif [[ $pilihan == 2 ]]; then
mulai
elif [[ $pilihan == 3 ]]; then
empas-fresh
elif [[ $pilihan == 4 ]]; then
empas-uncheck
elif [[ $pilihan == 5 ]]; then
empas-moontod
else
echo -e "${r}Pilih yang ada aja njeng"
banner
menu
fi
}

cek
menu
© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
