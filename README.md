# -EVENT-REVSCRIPT-VipSystem

**Observações:**

» **O sistema pode conter erros, então antes de reclamar, por favor reporte.**<br>
» Transformei esse script pra RevScript, compativel com a [OTBR](https://github.com/opentibiabr/otservbr-global.git).<br>
» Caso tiver alguma duvida ou ocorrer algum erro, abra um [Issues](https://github.com/brunomaidana97/-EVENT-REVSCRIPT-VipSystem/issues).<br>
» Caso queira contribuir ou corrigir algum erro, abra um [Pull requests](https://github.com/brunomaidana97/-EVENT-REVSCRIPT-VipSystem/pulls).
» Se esse script for de sua autoria, entre em contato comigo para ser adiciona os creditos.

1. **Como funciona?**

» *Sistema de vip, podendo criar acessos e beneficios somente para players vip.*<br>
  

2. **Como instalar?**

» *Primeiro execute essa MySQL query na sua database*

    ALTER TABLE `accounts`
        ADD COLUMN `viplastday` int(10) NOT NULL DEFAULT 0 AFTER `lastday`,
        ADD COLUMN `vipdays` int(11) NOT NULL DEFAULT 0 AFTER `lastday`;

» *Para instalar sem erro, basta jogar os scripts nos respectivos locais e adicionar o que falta.*<br>
» *Verifique as observações que estão dentro dos scripts.*<br>

» *Para adicionar exp ao player que for vip abra seu player.lua que fica em data/events/scripts.*<br>
» *Procure por function Player:onGainExperience(source, exp, rawExp) e adicione antes do return exp:*
<br>
```
-- Vip Exp
if self:isVip() then
  exp = exp * 1.2
end
```

3. **Creditos**

» *Créditos a Printer e Numm / Otland*
