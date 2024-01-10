db.tabPesquisa.Close;
db.tabPesquisa.ParamByName('IP_NRSEQUENCIA').AsInteger := StrToInt( edTexto.Text);
db.tabPesquisa.Open;

ShowMessage('O valor total é ' + db.tabPesquisaTOTAL.AsString);

tabPesquisa é o ibquery
db é o form do banco



como pegar a informação do edtext e jogar no sql

SELECT
SUM(IP.IP_VLTOTAL) AS TOTAL
FROM ITEMPEDIDO IP
INNER JOIN PEDIDO PE ON (PE.P_IDPEDIDO = IP.IP_IDPEDIDO )
WHERE IP.IP_NRSEQUENCIA =  :IP_NRSEQUENCIA


eu sou mto burro, era somente isso que ja tava certo
