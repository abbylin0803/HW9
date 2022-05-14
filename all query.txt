
-- question 1 
select employee.emp_no, employee.emp_title_id, title.titlename, employee.first_name, employee.last_name, sal.salary, dept_name
from title
join employee on 
employee.emp_title_id = title.title
join sal on 
employee.emp_no = sal.emp_no
join depemp on
depemp.emp_no = employee.emp_no
join dept on
dept.dept_no = depemp.dept_no;

-- question 2 
SELECT em.first_name, em.last_name, em.hire_date 
FROM employee as em
where hire_date >= '1986/01/01' AND  hire_date <= '1986/12/31' 

--question 3 
select deptmanager.dept_no, dept.dept_name, deptmanager.emp_no, employee.first_name, employee.last_name
from deptmanager
join dept on 
dept.dept_no = deptmanager.dept_no 
join employee on 
employee.emp_no = deptmanager.emp_no;


-- question 4 (shown in question 1 already, so it's the same query)
select employee.emp_no, employee.emp_title_id, title.titlename, employee.first_name, employee.last_name, sal.salary, dept_name
from title
join employee on 
employee.emp_title_id = title.title
join sal on 
employee.emp_no = sal.emp_no
join depemp on
depemp.emp_no = employee.emp_no
join dept on
dept.dept_no = depemp.dept_no;

-- question5 
SELECT em.first_name, em.last_name, em.hire_date, em.sex
FROM employee as em
where first_name = 'Hercules' AND last_name like 'B%';

-- question 6 
select employee.emp_no, employee.first_name, employee.last_name, dept_name
from employee
join depemp on
depemp.emp_no = employee.emp_no
join dept on
dept.dept_no = depemp.dept_no
where dept_name = 'Sales';

--question 7 
select employee.emp_no, employee.first_name, employee.last_name, dept_name
from employee
join depemp on
depemp.emp_no = employee.emp_no
join dept on
dept.dept_no = depemp.dept_no
where dept_name = 'Sales' or dept_name = 'Development';


-- question 8
select count(*), last_name 
from employee 
group by last_name
order by count desc; 