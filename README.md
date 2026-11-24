# Corporates Connect Project Manager
## The Plan

Who will use it: I will use this app as the founder of Corporates Connect to assign event and project tasks to ambassadors and event co-leads. This will keep event and project progress in one place, easy for everyone to track what needs to be done. I will ask one or more past ambassadors who are not in this course to try it.

What they choose or type, and what they see: When an ambassador or co-lead opens the app, they can choose "Tasks to Do" and select an event or project they’re assigned to. If they’re assigned to only one, the app can take them directly to it. They can see tasks to do and tasks completed, including additional details, due dates, and progress.

Which table holds real data, and where it comes from: A Python script will load public holiday data for Canada and the United States from the Nager.Date API into a public_holidays table. The data includes each holiday’s date, name, country, and applicable province or state. For example, the script can request Canadian holidays from https://nagerholidays.com/api/v4/Holidays/CA/2027 and U.S. holidays from https://nagerholidays.com/api/v4/Holidays/US/2027. The app can flag event dates that overlap a public holiday.

Which tables the answer comes from, and how they connect: The task list will use tasks, projects, and people. The query will connect tasks to projects using project_id, and connect each task’s assignee_id to people.person_id. It will use project_members to show the person’s role on the project and events to show event details. For event projects, it will compare the event date with public_holidays.

What the AI step does for the user: The AI step will help ambassadors promote an event. They can provide the event’s city, target audience, and theme to get promotion ideas and a starter list of local businesses or organizations to research and contact about promoting the event to young professionals and interns. Ambassadors can turn ideas they choose into assigned tasks and check that each business is a good fit before reaching out.