+++
title = "philosophers"
template = "project.html"
weight = 6
description = "philosophers"
+++

# Philosophers

Is an individual project about a classic problem in concurrent programming that
involves simulating a scenario where a group of philosophers sits around a table,
and each philosopher alternates between thinking, eating and sleeping.
The philosophers are represented as concurrent threads or processes, and they
interact with shared resources (forks) to eat, implementing synchronization mechanisms
to prevent conflicts and ensure proper resource sharing as mutex locks and semaphores
are used to avoid data races.

```
void
philo_eats(t_philo *philo, t_table *table)
{
	pthread_mutex_lock(&table->philo[philo->left_index].fork);
	state(philo, FORK);
	pthread_mutex_lock(&table->philo[philo->rigth_index].fork);
	state(philo, FORK);
	pthread_mutex_lock(&table->eat_check);
	state(philo, EAT);
	(philo->times_ate)++;
	philo->last_eat = get_time();
	pthread_mutex_unlock(&table->eat_check);
	ft_sleep(table->time_to_eat);
	pthread_mutex_unlock(&table->philo[philo->left_index].fork);
	pthread_mutex_unlock(&table->philo[philo->rigth_index].fork);
}
```

<div class="links">
	<div> <a target="blank" href="https://github.com/sebamiro/philosophers42">GitHub</a> </div>
	<div> <a target="blank" href="https://cdn.intra.42.fr/pdf/pdf/90306/en.subject.pdf">Subject</a> </div>
</div>
