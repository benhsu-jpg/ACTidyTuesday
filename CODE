# ACTidyTuesday
Animal Crossing Tidy Tuesday Project
Made by Ben Hsu (@benhsu_ on Twitter)


library(tidyverse)
critic <- readr::read_tsv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-05-05/critic.tsv')
user_reviews <- readr::read_tsv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-05-05/user_reviews.tsv')
items <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-05-05/items.csv')
villagers <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-05-05/villagers.csv')

villagers %>% 
  select(species, personality) %>% 
  arrange(species) %>% 
  group_by(species, personality) %>% 
  summarise(freq = n()) %>% 
  ggplot(aes(x = personality, y = species, color = freq, size = freq)) +
  geom_count() +
  scale_color_gradient(low="forest green",high="deepskyblue") +
  ggsave("actinytuesday.png",width=5, height=5)
