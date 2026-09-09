function dailyLog166() {
  const habits = [
    { name: "Read", completed: true },
    { name: "Exercise", completed: true },
    { name: "Code", completed: true },
    { name: "Drink Water", completed: false },
    { name: "Sleep Early", completed: true }
  ];

  const completed = habits.filter(habit => habit.completed).length;
  const consistencyRate = (completed / habits.length) * 100;

  const report = {
    date: new Date().toISOString().split("T")[0],
    totalHabits: habits.length,
    completedHabits: completed,
    missedHabits: habits.length - completed,
    consistencyRate: `${consistencyRate.toFixed(1)}%`,
    status: consistencyRate >= 80 ? "Great consistency" : "Keep improvin"
  };

  console.log("Daily Habit Report:", report);
}

dailyLog166();
