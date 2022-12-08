package com.example.students.service.impl;

import java.util.List;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import com.example.students.model.Students;
import com.example.students.repository.IStudentsRepository;
import com.example.students.service.IStudentsService;

@Service
public class StudentsService implements IStudentsService {

    @Autowired
    IStudentsRepository studentsRepository;

    @Override
    public Students insertStudents(Students students) {
        // TODO Auto-generated method stub
        return studentsRepository.insertStudents(students);
    }

    @Override
    public List<Students> getAllStudents() {
        // TODO Auto-generated method stub
        return studentsRepository.getAllStudents();
    }

    @Override
    public Students updateStudents(int id, Students students) {
        // TODO Auto-generated method stub
        return studentsRepository.updateStudents(id, students);
    }

    @Override
    public Students deleteStudents(int id) {
        // TODO Auto-generated method stub
        return studentsRepository.deleteStudents(id);
    }

}
