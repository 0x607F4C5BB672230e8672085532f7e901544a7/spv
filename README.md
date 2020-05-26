# spv

## block header

On garde le blockheader du dernier bloc, ainsi qu'un hash

Quand c'est un nouveau block on mets à jour le blockheader on vérifie la pow, on change le blockheader, et le hash devient sha(hash + blockheader)

Quand c'est un re-org on pars d'une pow donnée en argument, on vérifie qu'elle est dans le hash, on mets à jour le hash pour revenir la où on était et on appel la fonction d'en haut en boucle

On peut pas perdre ce qu'il y a avait dans la hash puisque c'est bien marqué en dur dans la blockchain même si c'est pas stocké dans le contrat

## liste des txs

Quand on push le block header on push aussi un hash de toutes les transactions. On mets de l'argent en jeu et quelqu'un peut challenge en donnant une transaction qui match avec la merkleroot du bloc et qui n'est pas dans ce hash la. Et inversement si il y a une tx en trop dans ce hash on peut contester, et si le mec ne donne pas la merkle proof on récupère l'argent

Au final on a la plus longue chaine mais si tu peux slash qqn c'est mort je pense

Néanmoins si quand on apporte une preuve de double dépense on récup la thune c'est bon

Chacun post tout sur bitcoin, et si le mec double dépense sur bitcoin pour que sa tx soit pas incluse on link les deux transactions ? Du coup pas besoin d'avoir la liste de txs ? Ca a l'air bancal 

En fait le truc bizarre c'est que ça s'arrête jamais. Si on s'autorise à poster les transactions des optimistics rollups ailleurs alors autant tout poster ailleurs ? Et on settle sur ethereum que plus tard

sinon avoirl a liste des txs d'un bloc ça servirait pour annuler un ordre de la marketplace au lieu de poster sur ethereum on poste ici et si t'essaye de match avec un ordre qui a déjà été post ailleurs tu perds ta thune
