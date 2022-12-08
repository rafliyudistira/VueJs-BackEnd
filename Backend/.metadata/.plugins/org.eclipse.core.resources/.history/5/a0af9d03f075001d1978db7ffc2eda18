package com.example.students.controller;

import java.util.List;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.CrossOrigin;
import org.springframework.web.bind.annotation.DeleteMapping;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.PutMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

import com.example.students.model.Students;
import com.example.students.service.IStudentsService;

@RestController
@CrossOrigin(origins = "http://localhost:8080")
@RequestMapping("/api/students")
public class StudentsController {

    @Autowired
    IStudentsService studentsService;

    @PostMapping("/insert")
    public Students insertStudents(@RequestBody Students students) {
        return studentsService.insertStudents(students);
    }

    @GetMapping("/getAll")
    public List<Students> getAllStudents() {
        return studentsService.getAllStudents();
    }

    @PutMapping("/update/{id}")
    public Students updateStudents(@PathVariable int id, @RequestBody Students students) {
        return studentsService.updateStudents(id, students);
    }

    @DeleteMapping("/delete/{id}")
    public Students deleteStudents(@PathVariable int id) {
        return studentsService.deleteStudents(id);
    }
}
