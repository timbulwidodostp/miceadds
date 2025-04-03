# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Cluster robust standard errors for linear models and general linear models Use lm.cluster And glm.cluster (miceadds) With (In) R Software
install.packages("miceadds")
install.packages("sandwich")
library("miceadds")
miceadds = read.csv("https://raw.githubusercontent.com/timbulwidodostp/miceadds/main/miceadds/miceadds.csv",sep = ";")
# Estimation Cluster robust standard errors for linear models and general linear models Use lm.cluster And glm.cluster (miceadds) With (In) R Software
lm.cluster <- miceadds::lm.cluster(data=miceadds, formula=read ~ hisei + female, cluster="idschool")
coef(lm.cluster)
vcov(lm.cluster)
summary(lm.cluster)
miceadds$highmath <- 1 * (miceadds$math > 600)
glm.cluster <- glm.cluster(data = miceadds, formula = highmath ~ hisei + female, cluster = "idschool", family="binomial")
coef(glm.cluster)
vcov(glm.cluster)
summary(glm.cluster)
# Cluster robust standard errors for linear models and general linear models Use lm.cluster And glm.cluster (miceadds) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
